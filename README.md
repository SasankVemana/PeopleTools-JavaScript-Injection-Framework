PeopleTools-JavaScript-Injection-Framework:
JavaScript Injection Framework for PeopleTools 8.55+ using Oracle JET (requireJS)

https://pe0ples0ft.blogspot.com/p/javascript-injection-framework.html

Documentation on Updates, Bugs and Fixes:
https://pe0ples0ft.blogspot.com/2019/03/javascript-injection-framework-updates.html

JavaScript Injection Framework:
- Add one line customization to PT_UTIL (at the very end) which helps with injecting our framework (via CSK_FL_BOOTSTRAP_JS) to all pages across the application.
%include(CSK_FL_BOOTSTRAP_JS);
- CSK_FL_BOOTSTRAP_JS is a javascript that contains several helper functions, includes CSK_INJECT_JS (serves as the configuration for adding javascripts), loads RequireJS (and it's configuration) and invokes a function in CSK_INJECT_JS as callback.
- CSK_INJECT_JS serves as an abstracted configuration script which we can use to load other custom javascript objects as per our requirements.

Additional Notes:
- Custom IScript for IScript_CSK_GET_IMG function is also provided in this project.
- CSK_JQUERY_1_7_2_JS is a custom HTML object with contents of jQuery 1.7.2.

For More Details:
https://pe0ples0ft.blogspot.com/2016/06/peopletools-855-using-oracle-jet-jquery.html

Troubleshooting Tips:
- If you run into issues with loading of Oracle JET - javascript libraries, then check the web server to see if the version number in the library path is accurate. For example, PeopleTools 8.56 uses Oracle JET version 2.1.0. This means that the jQuery version available will be 3.1.0. If we are referencing older versions of jQuery which no longer exist in Oracle JET, then we need to update the path to point to the 3.1.0 version. Here is sample of CSK_REQUIRE_CFG_JS with appropriate path for jQuery: https://gist.github.com/SasankVemana/83cc903f1eee08c7f8aab8911ec511ee
