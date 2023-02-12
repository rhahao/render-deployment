# Render Deployment

A GitHub Action to trigger deployment in Render.

## Example Usage

```yaml
name: Trigger Render Deployment
on:
  push:
    branches:
      - main
jobs:
  main:
    name: Deploy to Render
    runs-on: ubuntu-latest
    steps:
      - name: Trigger deployment
        uses: sws2apps/render-deployment@main #consider using pin for dependabot auto update
        with:
          serviceId: ${{ secrets.RENDER_SERVICE_ID }}
          apiKey: ${{ secrets.RENDER_API_KEY }}
          multipleDeployment: false #optional, default true
```
