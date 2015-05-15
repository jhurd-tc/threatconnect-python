threatconnect-python
=========================

The threatconnect-python project is a part of the ThreatConnect SDK.  This module implement methods that can be used to pull data from the ThreatConnect V2 REST API.  This module provides method for pushing and pulling data via the API.

Requirements
------
The threatconnect-python project can run under Python 2.6+.
Python 2.x requirements:
 * Requests 2.7+ module (http://docs.python-requests.org/en/latest/).
 * enum34 module (https://pypi.python.org/pypi/enum34).
 
Python 3.x support coming soon.

API credentials with a ThreatConnect instance is required to run this module.  Please see http://www.threatconnect.com/product/threatconnect_API for more information on obtaining API credentials.  

Installation
-----
cd threatconnect-python
python setup.py install

To automatically pull prerequisites.
pip setup.py install
  
Instantiation
-----

```
from threatconnect import ThreatConnect

tc = ThreatConnect(api_access_id, api_secret_key, api_default_org, api_base_url, api_max_results)

owners = tc.owners()
owners.retrieve()

if owners.get_status().name == "SUCCESS":
    for owner in owners():
        print(owner)
```

For more examples see the examples folder under the project.

Contact
-----
If you have any questions, bugs, or requests please contact support@threatconnect.com

