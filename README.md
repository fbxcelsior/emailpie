# A simple email validation API.

Give us an email and we make sure its legit. If not, you'll find out why.


### Features

* Uses gevent for fastness.
* Normal regex based check.
* Ensures DNS records exist for the mail exchange.
* Suggest fixes to common misspellings. lulz@gnail.com -> did you mean lulz@**gmail**.com.
* Throttled requests by IP (redis based).
* **TODO:** Fix timeout failure...


### Install/Usage

**Make sure redis is installed and running on the standard ports!**

1. `git clone git@github.com:bryanhelmig/emailpie.git`
2. `cd emailpie`
3. `mkvirtualenv emailpie`
4. `pip install -r requirements`
5. `python rundev.py`
6. Visit http://localhost:5000/v1/check?email=test@gmail.com
