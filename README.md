# Crop-Recommendation

This is my crop recommendation project where multiple models are compared and a website is made using Flask to deploy the project


1. Modify Flask to Bind to All Interfaces
In your app.py (or wherever you start your Flask app), make sure you are binding to 0.0.0.0 instead of 127.0.0.1. This allows the app to be accessed externally.

Find this line:
app.run(debug=True)

Replace it with:
app.run(host='0.0.0.0', port=int(os.environ.get("PORT", 5000)))

This ensures Flask will bind to 0.0.0.0 (meaning all network interfaces) and listen on a port specified by the environment variable PORT. Render dynamically assigns a port to your app, so using os.environ.get("PORT", 5000) will allow it to work correctly.
