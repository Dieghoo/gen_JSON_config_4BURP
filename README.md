# gen_JSON_config_4BURP
A simple script that accepts a list of regexes to be passed to Burp Suite. The initial idea is to pipe the regex-scope-burp´s output to generate an array of possible JSON structures to be inserted into a output file named scope_config.json to then placed into Burp Config Files.


C program to generate a Burp Suite scope configuration JSON file from a list of domain names.

This program reads in a list of domain names from a text file and generates a Burp Suite scope configuration JSON file. The JSON file includes a common configuration for all domains, which is defined by the regex_pattern variable in the code. The $abfut placeholder in the regex_pattern string is replaced with each domain name from the input file to create a separate configuration for each domain.
Contributors

    OpenAI
    dhParadox

Usage

To use this program, you will need a C compiler installed on your system.

To compile the program, run the following command:

bash

gcc generate_scope_config.c -o generate_scope_config

To generate the scope configuration JSON file, run the following command:

bash

./generate_scope_config <input_file>

Replace <input_file> with the name of the text file containing the list of domain names. The generated JSON file will be written to a file named scope_config.json in the current directory.
Customization

You can customize the common configuration for all domains by modifying the regex_pattern variable in the code. The default configuration is:

json

{
  "enabled": true,
  "file": "^/\\\\.*",
  "host": "$abfut",
  "port": "(?:\\\\b(?:[0-9]|[1-9]\\\\d|1\\\\d{2}|2[0-4]\\\\d|25[0-5])\\\\b)*",
  "protocol": "any"
}

The $abfut placeholder in the host field will be replaced with each domain name from the input file to create a separate configuration for each domain.
License

This program is licensed under the MIT License. See the LICENSE file for details.
