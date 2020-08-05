# MusicStatisticReader: YouTube Music
Get your YouTube Music listening statistics

Precompiled JARs can be found under [Releases](https://github.com/TheDutchMC/MusicStatisticReader/releases) 

## Usage
Run the following command in cmd or a terminal in the directory where ``YTmusicReader.jar`` is located:  
``java -jar YTmusicReader.jar <path to My Activity.json> [year] [max output]``

- <...>`` means required.
- [...]`` means optional, though to include max output you need to specifiy a year!

If the year is not provided, it will default to the current year.
If max output is not provided, it wil ldefault to 10

**NOTE: The path NEEDS to be in double quotes!**

## Getting your statistics
1. Go to [Google Takeout](https://takeout.google.com/settings/takeout)
2. Under "Select data to include" select "Deselect all"
3. Scroll down until you see "YouTube and YouTube Music", check it to be included.
4. Under "YouTube and YouTube Music", select "Multiple Formats", make sure it is set to JSON
5. Under "YouTube and YouTube Music", select "All YouTube data included", in this menu select "Deselect all", and then only select "history"
6. Scroll to the bottom of the page and select "Next Step
7. Set "Frequency" to "Export once"
8. Set File type to .zip, and File size to 2GB
9. Press "Create Export"
10. You will receive an email from Google shortly with a download link. This will be a ZIP file.
11. In this ZIP file you need to navigate to ``Takeout/My Activity/Google Play Music/``. You need to copy out ``My Activity.json``.

## Compiling from source
For Windows:
```
gradlew shadowJar
```

For Linux:
```
chmod +x gradlew
./gradlew shadowJar
```

For both distributions to JAR can be found at ``build/libs/GmusicReader-all.jar``
