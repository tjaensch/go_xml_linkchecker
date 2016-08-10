+++ CONCURRENT XML LINKCHECKER +++

WHAT DOES IT DO?
Check all http:// and https:// links in XML files in directory the tool is run in, report back the server responses received from the checked links and log the failed responses (everything other than "200 OK") to a linkchecker_bad_links_log file in the current working directory

PREREQUISITES
The program uses Bash and cURL commands under the hood and will not work if Bash and/or cURL are not installed in the environment it's run in

HOW TO RUN IT?
Run "go run linkchecker.go" in the directory with the XML files with links to be checked (or "go build linkchecker.go" and then execute the binary "./linkchecker")

CONCURRENCY
The tool currently runs on 5 XML files concurrently but that's configurable