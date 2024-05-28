# Going Live checklist


## Design
Contents are consistent

## Clean-up
Remove all unused packeges, files, images, css

## Security
### Zero vulnerabilities
Make sure all reported security vulnerabilities are removed
#### NPM
use `npm audit` to check for known vulnerabilities
#### SonarQube
It not only analyize code for cyclomertic complexity but also report leakages, and security vulnerabilities in the codebase.

## Testing

### Functional testing
Do end to end functional testing to ensure all features are working as per the expectations

### Security testing
Test your application for code level breaches (SQL Injection, NoSQL Injection)
* Use automated tools to perform test analysis
* Perform penetration testing
* Test your infrastruture for breaches and run expolit scans
* Remove keys, secrets or any passwords from codebase, also change them on actual source
* Passwords must be difficult to guess - better to write a songe in your own language `Qameez Teri Kaali ni sohnay phulaan waali` to prent from dictionay attacks. 

### Trivy
Use Trivy to scan vulnerabilities in your dependencies/packages or docker image


#images are compressed, z-compression enabled
#use production version of reactjs
