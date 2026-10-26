<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://ai.google.dev/static/site-assets/images/share-ais-513315318.png" />
</div>

# Run and deploy your AI Studio app

This contains everything you need to run your app locally.

View your app in AI Studio: https://ai.studio/apps/1f73fb9f-911e-45d3-9ede-3b0cf17a24f7

## Run Locally

**Prerequisites:**  Node.js


1. Install dependencies:
   `npm install`
2. Set the `GEMINI_API_KEY` in [.env.local](.env.local) to your Gemini API key
3. Run the app:
   `npm run dev`


## Image URL and existing Apps Script deployment fix

- The frontend default Apps Script URL now points to the user's existing `/exec` deployment.
- If browser local storage contains the previously bundled default deployment ID, the app migrates that one stale URL to the existing deployment. Other custom URLs are preserved.
- Product image loading still uses the existing Google Drive thumbnail URL and the existing fallback sequence; sharing permissions on each image file must still permit the intended audience to view it.
- To publish the backend changes, edit the existing Apps Script deployment and choose **New version**. Do not create a new deployment if the old URL must remain unchanged.
