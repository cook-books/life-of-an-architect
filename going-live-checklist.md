# Going Live checklist


## Design
* Contents is consistent throughout the platform
* Check for crossbrowser compatibility on both mobile and desktop devices (Firefox, Edge, Safari, Chrome)
* Make sure images are compressed
* Load time should be under 2-3 seconds
* CSS/JavaScript is minified/Compressed
* Use 1 or 2 fonts only, and remove uncessary fonts
* Be consistent on number of colors
* Use web safe colors in your design
* 

## Clean-up
Remove all unused packeges, files, images, css

## Security
### Zero vulnerabilities
Make sure all reported security vulnerabilities are removed
#### NPM
use `npm audit` to check for known vulnerabilities
#### SonarQube
It not only analyize code for cyclomertic complexity but also report leakages, and security vulnerabilities in the codebase.

## Network
### Gzip compression
Enable a compression at the webserver level so that all data communication happened in minified way which will reduce the usgae of bandwidth and increase network delivery speed.
### Cache
Ensure static contents are cached approproately, which means if same content is requested browser can serve that locally, and it also mean if content changes on server the browser should not present outdated contents (Comment/Contact to know more about this)

## Testing
Perform all testing on actual environement and not on localhost

### Functional testing
Do end to end functional to ensure all features are working as per the expectations

### Decorate Errors
Please make sure no error is shown to the customer like 
* Database `db_banking` app does not exist
* User `root` is unable to access using password
* Hide any information which revelas details about code, database or file structure
* None of your directories should be listable (Sepcailly for websites)

### Security testing
Test your application for code level breaches (SQL Injection, NoSQL Injection)
* Use automated tools to perform test analysis
* Perform penetration testing
* Test your infrastruture for breaches and run expolit scans
* Remove keys, secrets or any passwords from codebase, also change them on actual source
* Passwords must be difficult to guess - better to write a songe in your own language `Qameez Teri Kaali ni sohnay phulaan waali` to prent from dictionay attacks. 

### Trivy
Use Trivy to scan vulnerabilities in your dependencies/packages or docker image

## Limiting
### Data Limiting
Please ensure none of the logic load data infinitely, `"Select * from products"`, a developer may think we never have too much products and hence Pagingation or limiting is not required, attackers usually use this technique to overload your database, always has a max limit (max 100 records) and every request must include limit 25 records per page, if not provided then fallback to 20 records per page.
### Rate limiting
Peformance test your application to find optimum number of a specific hardware, and then based on your user base rate-limit you requests



#images are compressed, z-compression enabled
#use production version of reactjs
