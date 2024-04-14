[![Build Status](https://travis-ci.org/lasconic/nwc2musicxml.svg?branch=master)](https://travis-ci.org/lasconic/nwc2musicxml)

The primary goal of this project is to provide a library to convert NWC scores to MusicXML. Then, Noteworthy users will be able to share their scores with others scorewriters, especially free ones such as [MuseScore](https://musescore.org). For the time being, the library supports only NWCtxt and you need a copy of NoteWhorthy composer to save a NWC file to NWCtxt.

The converter is also available online as a webservice on Google App Engine at https://nwc2musicxml.appspot.com/

If you find the software useful you can [donate](https://paypal.me/lasconic).

Features
==

* Multiple staves & voices, invisible staff not exported
* Notes, rests, accidentals, dots, time signature
* Key signature (not the customized ones)
* Clefs included octave shift
* Tie & slurs, triplets
* Line breaks
* Lyrics
* Metadata: Title, author, lyricist, copyright
* Staccato, tenuto & accent, noteheads
* Dynamics (mf, p ...) & custom texts
* Midi info for staff
* Beaming
* Flow control : Coda, Segno, ...


Not yet supported
==
* Chord symbols, grace notes
* Dynamic variation
* Layout information

How to Run
==
* Download this repo to your machine. You can use git clone if you have git installed, otherwise download the zip file and unzip it.
* Install a current JDK and Apache Ant build tool, and make sure both the JDK and Ant is configured in your path environment variable.
* Open a terminal, then cd to the project folder.
* run the following commands: 
    ```ant clean``` (optional)
    ```ant build```
    ```ant test``` (optional)
    ```ant package```

The package command will create a .jar file in the /build folder called ***NwcTxt2MusicXML.jar***. This file should be portable to any device with Java installed.

To convert a .nwctxt file into xml (actually musicXML format), run the command:
```java -jar NwcTxt2MusicXML.jar myInputFile.nwctxt myOutputFile.xml```

Note: if you're not running the command from the same folder as the .jar file, then specify the full path.

Thanks to [Noteworthy Software](http://www.noteworthysoftware.com/) for giving me a free licence for testing purpose.
