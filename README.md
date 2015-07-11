#Alert Plus

A modal alert box using jquery and bootstrap. Has message and details section.

##Usage

You must include bootstrap javascript and css and jquery javascript in your document. Also include javascript and css of alertplus. Then to use within your javascript simply do ...

    alertplus.alert(message, details);

... or for errors ...

    alertplus.error(error);

TODO: Talk about the different error formats excepted.

##Test

See test.html for testing of the dialog. Note, this is a computed file from the test.jade. If you wish to add tests to it you must edit the test.jade file and then run ...

    jade < test.jade > test.html
    
To install and use jade you must have node installed and then do ...

    npm install jade --global
    

