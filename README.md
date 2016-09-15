
Please don't use this yet!! 

The data in this scraper is partly faked - the start date is set to 1.1.16 and all MPS are current only. This will be updated once I learn to use mechanize to do it properly... 

This parser repeats the scrape of the MP list, and then reads out information for lower house MPs only, into the fields expected by OpenAustralia's parser.

Those two csv files need to be generated separately to get their own URLs, so that forked openaustralia parsers can pull them into a database. 

scraper #1: List of MPS - https://morph.io/alisonkeen/SA\_MHRS\_for\_OA\_input
fields {id, saparl ID, full name}
destination: /var/www/openaustralia/openaustralia-parser/data/people.csv

scraper #2: List of MHRs - https://morph.io/alisonkeen/SA\_members\_for\_OA\_parser
fields {id, id2, Name, Electorate, State/Territory(?), Start date, Election type, End date, reason, Most recent party}
destination: /var/www/openaustralia/openaustralia-parser/data/representatives.csv

scraper #3: List of Senators - (coming soon)
fields {id, id2, Name, Electorate, State/Territory(?), Start date, Election type, End date, reason, Most recent party}


This is a scraper that runs on [Morph](https://morph.io). To get started [see the documentation](https://morph.io/documentation)
