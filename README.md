# munki-rosetta
munki nopkg that installs rosetta if initial push fails


Package receipt checking was failing since the reciept created for Rosetta does not include a version number.
this `nopkg` checks receipts for rosetta, and if not found, uses postinstall script to call the install.

it's in my site_default manifest with a condition of `arch == "arm64"`
