PeopleTools-JavaScript-Injection-Framework:
JavaScript Injection Framework for PeopleTools 8.55+ using Oracle JET (requireJS)

https://pe0ples0ft.blogspot.com/p/javascript-injection-framework.html

JavaScript Injection Framework:
- Add one line customization to PT_UTIL (at the very end) which helps with injecting our framework (via CSK_FL_BOOTSTRAP_JS) to all pages across the application.
%include(CSK_FL_BOOTSTRAP_JS);
- CSK_FL_BOOTSTRAP_JS is a javascript that contains several helper functions, includes CSK_INJECT_JS (serves as the configuration for adding javascripts), loads RequireJS (and it's configuration) and invokes a function in CSK_INJECT_JS as callback.
- CSK_INJECT_JS serves as an abstracted configuration script which we can use to load other custom javascript objects as per our requirements.

Useful Links:
https://pe0ples0ft.blogspot.com/2016/06/peopletools-855-using-oracle-jet-jquery.html

