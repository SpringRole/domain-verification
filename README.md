# domain-verification
This module help you to verify domain ownership.

## Install

    $ npm install domain-verification

## Usage

    const domainVerification = require('domain-verification');
    domainVerification.html(domain_url,domain_html_name,hash_value);
    domainVerification.txt(domain_url,domain_key,domain_value);
    domainVerification.metatag(domain_url,domain_key,domain_value);
    domainVerification.all(domain_url,domain_key,domain_value,domain_html_name,hash_value);

    We are supporting Promise. 
    
## 1. html:
    
    Verify by uploading a specific HTML to a given domain.

  ### Parameters:
  * domain_url: The URL where the html file can be formed (http://example.com).
  * domain_html_name: The name of the html file expected at 'domain_url'
  * hash_value: The value in the html file body
    
  ### Asssumptions:
  * The domain to be verified has the HTML file specified in the url specified by 'domain_url'.
  * The filename is of the form: 'domain_html_name'.html, eg. 'domainVerified-1233ask.html'

## 2. txt:
    Verify by Txt in the DNS of the domain:
    
### Parameters:
* domain_url: The URL of the domain that has the Txt file added
* domain_key: The Txt key
* domain_value: The Txt value

## 3. metatag:
    Verify by metatag information of  a domain:
    
  ### Parameters:
  * domain_url: The URL of the domain containing the metatag
  * domain_key: The meta tag key/name
  * domain_value: The value of the meta tag key/name

## 3. all:
    This methods call all the above 3 function and give you the result:
    
