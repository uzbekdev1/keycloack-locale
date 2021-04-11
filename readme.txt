pg create new database keycloak
replace exsting fiels to source
cd keycloak/bin
./add-user-keycloak.bat -r master -u admin -p web@1234
./kcadm.bat config credentials --server http://localhost:8080/auth --realm master --user admin
./kcadm.bat update realms/master -s sslRequired=NONE
./standalone.bat -b 0.0.0.0 -Djboss.bind.address=0.0.0.0 -Djboss.bind.address.management=0.0.0.0