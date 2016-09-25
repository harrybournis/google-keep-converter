This script lets you scrape and convert Google Keep notes into sensible, reusable file formats, such as JSON and CSV.

Installation:

1. Install Node.js on your machine
2. Run `npm install`
3. Get your Google Keep data via Google Takeout -- there is no other way for now -- and extract the ./Takeout/Keep/ folder.

Usage: `node index.js [options]`

The output is saved to keep-notes-[timestring].json: in chronological order, UTF8-encoded, with \n linebreaks. 

Options:

| Command | Description |
| --- | --- |
| -h, --help | output usage information |
| -f, --fix | fix naming of HTML files (workaround for Google Takeout bug) |
| -c, --csv | save to keep-notes-[timestring].csv (additionally) |

Note:
If you have a bunch of files without proper file extension in your Keep folder, you have run into a Google Takeout bug.
It seems that if a note title ends in a period and digit (e.g. "Ideas for Industry 5.0"), the filename is truncated.
Use the --fix option to give those files an ".html" extension, to be properly processed by this script.