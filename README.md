# Auto_link-ExB_widget
 
📘 Auto Link Widget for ArcGIS Experience Builder
This widget automatically redirects specific users to a predefined link when they open the application — no UI, no buttons, just smooth logic.


🚀 Features
✅ Automatic redirection on page load
✅ Redirect only for matching usernames (supporting multiple)
✅ Supports links to:

External websites (https://example.com)

Pages inside the Experience Builder app

✅ Skips redirection in builder/edit mode
✅ Works in both local and published environments

⚙️ How It Works
When a user opens the app, the widget checks the username from SessionManager.

If this user matches any value from the configured Username list:
    They are redirected to the configured Link.
    If the link is an Experience Builder Page, the current ?id=... context is preserved.

🛠 Configuration

Setting	    Description
Username  	One or multiple usernames allowed access. Separate by comma, space, or both.
farhod, khadicha, john doe
Redirect Link   	Use the Link Selector to choose a page or enter a full URL (external or internal).

🔐 Username Format
The username is matched case-insensitively, and supports multiple entries like:

khadicha, Farhog   johnDoe
All of these are normalized to lowercase internally.

✅ Example Use Case
Want to redirect internal editors or admins like john,editor1 directly to a dashboard page Page-Admin upon login?
Set the usernames, link to Page-Admin, and drop this widget into a hidden section of the app — done!