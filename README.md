name: Deploy Profile API to GitHub Pages

# Deploys a lightweight API for dynamic profile content
on:
  schedule:
    - cron: '0 */6 * * *'  # Every 6 hours
  workflow_dispatch:
  push:
    branches:
      - main
    paths:
      - 'api/**'
      - '.github/workflows/deploy-api.yml'

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    
    permissions:
      contents: write
      pages: write
      id-token: write
    
    steps:
      # Step 1: Checkout repository
      - name: Checkout Repository
        uses: actions/checkout@v4
      
      # Step 2: Setup Node.js for API generation
      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: '20'
      
      # Step 3: Create API directory structure
      - name: Create API Structure
        run: |
          mkdir -p api/data
          mkdir -p api/endpoints
      
      # Step 4: Generate dynamic API data
      - name: Generate API Data
        run: |
          # Create skills.json
          cat > api/data/skills.json << 'EOF'
          {
            "languages": ["Python", "JavaScript", "SQL", "HTML", "CSS"],
            "frameworks": ["React", "Node.js", "Flask", "Bootstrap"],
            "tools": ["Git", "VS Code", "Power BI", "Jupyter", "Linux"],
            "specializations": ["Machine Learning", "Data Analysis", "Full Stack Development"]
          }
          EOF
          
          # Create projects.json
          cat > api/data/projects.json << 'EOF'
          {
            "featured": [
              {
                "name": "Loan Data Analysis",
                "tech": ["Python", "Pandas", "Machine Learning"],
                "description": "Advanced data analytics for loan approval prediction",
                "stars": 0,
                "url": "https://github.com/Har-dik25"
              },
              {
                "name": "AI Traffic Congestion Analysis",
                "tech": ["Python", "OpenCV", "TensorFlow", "YOLOv5"],
                "description": "Smart traffic management using computer vision",
                "stars": 0,
                "url": "https://github.com/Har-dik25"
              },
              {
                "name": "LegalLens AI",
                "tech": ["Python", "NLP", "spaCy", "Flask"],
                "description": "AI-powered legal document analyzer",
                "stars": 0,
                "url": "https://github.com/Har-dik25"
              }
            ]
          }
          EOF
          
          # Create stats.json with current timestamp
          cat > api/data/stats.json << EOF
          {
            "last_updated": "$(date -u +'%Y-%m-%dT%H:%M:%SZ')",
            "github": {
              "username": "Har-dik25",
              "profile_url": "https://github.com/Har-dik25"
            },
            "metrics": {
              "total_projects": 10,
              "total_commits": 0,
              "followers": 0,
              "following": 0
            }
          }
          EOF
          
          # Create activity.json
          cat > api/data/activity.json << 'EOF'
          {
            "current_focus": [
              "Advanced Deep Learning & Transformers",
              "AWS Certified Machine Learning Specialty",
              "Building end-to-end ML pipelines",
              "Contributing to Open Source ML projects"
            ],
            "achievements": [
              {"milestone": "Built 10+ real-world projects", "year": 2024},
              {"milestone": "Solved 200+ coding problems", "year": 2024},
              {"milestone": "Created 5 Power BI dashboards", "year": 2023},
              {"milestone": "Deployed 3 production models", "year": 2024}
            ]
          }
          EOF
      
      # Step 5: Create API index page
      - name: Create API Documentation
        run: |
          cat > api/index.html << 'EOF'
          <!DOCTYPE html>
          <html lang="en">
          <head>
              <meta charset="UTF-8">
              <meta name="viewport" content="width=device-width, initial-scale=1.0">
              <title>Hardik Choudhary - Profile API</title>
              <style>
                  * { margin: 0; padding: 0; box-sizing: border-box; }
                  body {
                      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
                      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
                      color: #fff;
                      padding: 40px 20px;
                      min-height: 100vh;
                  }
                  .container {
                      max-width: 900px;
                      margin: 0 auto;
                      background: rgba(255, 255, 255, 0.1);
                      backdrop-filter: blur(10px);
                      border-radius: 20px;
                      padding: 40px;
                      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
                  }
                  h1 { font-size: 3em; margin-bottom: 10px; }
                  .subtitle { font-size: 1.2em; opacity: 0.9; margin-bottom: 30px; }
                  .endpoint {
                      background: rgba(255, 255, 255, 0.15);
                      padding: 20px;
                      margin: 15px 0;
                      border-radius: 10px;
                      border-left: 4px solid #4ade80;
                  }
                  .endpoint h3 { margin-bottom: 10px; color: #4ade80; }
                  .endpoint code {
                      background: rgba(0, 0, 0, 0.3);
                      padding: 8px 12px;
                      border-radius: 5px;
                      display: block;
                      margin: 10px 0;
                      font-size: 0.9em;
                  }
                  .badge {
                      display: inline-block;
                      background: #4ade80;
                      color: #000;
                      padding: 5px 15px;
                      border-radius: 20px;
                      font-size: 0.8em;
                      font-weight: bold;
                      margin-right: 10px;
                  }
                  a { color: #4ade80; text-decoration: none; }
                  a:hover { text-decoration: underline; }
              </style>
          </head>
          <body>
              <div class="container">
                  <h1>🚀 Profile API</h1>
                  <p class="subtitle">Dynamic endpoints for Hardik Choudhary's GitHub profile</p>
                  
                  <div class="endpoint">
                      <h3>📊 Skills</h3>
                      <span class="badge">GET</span>
                      <code>https://Har-dik25.github.io/Har-dik25/api/data/skills.json</code>
                      <p>Returns all technical skills, languages, frameworks, and tools</p>
                  </div>
                  
                  <div class="endpoint">
                      <h3>💼 Projects</h3>
                      <span class="badge">GET</span>
                      <code>https://Har-dik25.github.io/Har-dik25/api/data/projects.json</code>
                      <p>Returns featured projects with descriptions and tech stack</p>
                  </div>
                  
                  <div class="endpoint">
                      <h3>📈 Stats</h3>
                      <span class="badge">GET</span>
                      <code>https://Har-dik25.github.io/Har-dik25/api/data/stats.json</code>
                      <p>Returns GitHub statistics and metrics</p>
                  </div>
                  
                  <div class="endpoint">
                      <h3>🎯 Activity</h3>
                      <span class="badge">GET</span>
                      <code>https://Har-dik25.github.io/Har-dik25/api/data/activity.json</code>
                      <p>Returns current focus areas and achievements</p>
                  </div>
                  
                  <hr style="margin: 30px 0; border: none; border-top: 1px solid rgba(255,255,255,0.2);">
                  
                  <p style="text-align: center; opacity: 0.8;">
                      Made with ❤️ by <a href="https://github.com/Har-dik25">Hardik Choudhary</a>
                  </p>
              </div>
          </body>
          </html>
          EOF
      
      # Step 6: Setup GitHub Pages
      - name: Setup Pages
        uses: actions/configure-pages@v4
      
      # Step 7: Upload artifact
      - name: Upload Artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: 'api/'
      
      # Step 8: Deploy to GitHub Pages
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
      
      # Step 9: Summary
      - name: Deployment Summary
        run: |
          echo "## 🚀 API Deployment Complete!" >> $GITHUB_STEP_SUMMARY
          echo "" >> $GITHUB_STEP_SUMMARY
          echo "Your Profile API is now live at:" >> $GITHUB_STEP_SUMMARY
          echo "" >> $GITHUB_STEP_SUMMARY
          echo "🔗 **https://Har-dik25.github.io/Har-dik25/api/**" >> $GITHUB_STEP_SUMMARY
          echo "" >> $GITHUB_STEP_SUMMARY
          echo "### Available Endpoints:" >> $GITHUB_STEP_SUMMARY
          echo "- Skills: \`/api/data/skills.json\`" >> $GITHUB_STEP_SUMMARY
          echo "- Projects: \`/api/data/projects.json\`" >> $GITHUB_STEP_SUMMARY
          echo "- Stats: \`/api/data/stats.json\`" >> $GITHUB_STEP_SUMMARY
          echo "- Activity: \`/api/data/activity.json\`" >> $GITHUB_STEP_SUMMARY
