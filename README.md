#Alert Plus

A modal alert box using jquery and bootstrap. Has message and details section.

##Requirements
* Bootstrap 3
* JQuery

##Usage
[See it in action](https://cdn.rawgit.com/crowmagnumb/alertplus/master/test/test.html)

You must include bootstrap javascript and css and jquery javascript in your document. Also include javascript and css of alertplus. Then to use within your javascript simply do

    alertplus.alert(message);
    
If you have secondary information to relay you can do

    alertplus.alert(message, details);

The details section will be behind an expand button and within a scroll so can be quite lengthy if need be.

Both message and details can be strings or html.

To display errors you can just do

    alertplus.error(error);

Where error can be of the following types:

* string (message)
* {message: message, stack: stack}
* error response from ajax call

where stack is rendered as details in the alert call are above.

Also there is the confirm option. e.g.

    alertplus.confirm(message, title, danger)
    .then(function() {
        doSomething();
    });
    
where danger is a boolean that if true just makes the message more red as a warning. Currently it is hard-coded to have just an OK and Cancel button. If OK is called then the returned promise from the confirm call is resolved (with no value) and if Cancel is chosen it is rejected.

##Test

See test.html for testing of the dialog. Note, this is a computed file from the test.jade. If you wish to add tests to it you must edit the test.jade file and then run ...

    jade < test.jade > test.html
    
To install and use jade you must have node installed and then do ...

    npm install jade --global
    

