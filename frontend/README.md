# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Debugging API Errors

If you encounter errors like `Request failed with status code 404`, follow these steps:

1. **Verify the API Endpoint**:  
   Ensure the API endpoint in your frontend matches the backend route. For example:
   ```javascript
   const API_BASE_URL = 'http://localhost:5000'; // Replace with your backend URL
   const endpoint = `${API_BASE_URL}/api/signup`; // Ensure this matches the backend route
   ```

2. **Check Backend Logs**:  
   Look at the backend server logs to confirm if the request is reaching the server and if the route exists.

3. **Test the Endpoint**:  
   Use tools like Postman or `curl` to test the backend endpoint directly.

4. **Cross-Origin Requests**:  
   If the backend is running on a different domain or port, ensure CORS is configured correctly on the backend.

5. **Network Tab in Browser**:  
   Open the browser's developer tools and check the Network tab to inspect the request and response details.

## Setting Up Google Maps

To enable Google Maps functionality, ensure you have a valid API key from the Google Cloud Console. Add the key to your `.env` file as follows:

```
VITE_GOOGLE_MAPS_API_KEY=YOUR_GOOGLE_MAPS_API_KEY
```

Replace `YOUR_GOOGLE_MAPS_API_KEY` with your actual API key. Ensure the following APIs are enabled in your Google Cloud Console:
- Maps JavaScript API
- Places API
- Geocoding API
- Distance Matrix API
