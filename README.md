Opauth-GitLab
=============
[Opauth][1] strategy for GitHub authentication.

Implemented based on http://doc.gitlab.com/ce/integration/oauth_provider.html using OAuth2.

Opauth is a multi-provider authentication framework for PHP.

Demo: http://opauth.org/#gitlab

Getting started
----------------
1. Install Opauth-GitLab:
   ```bash
   cd path_to_opauth/Strategy
   git clone git://github.com/uzyn/opauth-gitlab.git GitLab
   ```

2. Register a GitLab application at https://github.com/settings/applications/new
   - Enter URL as your application URL (this can be outside of Opauth)
   - Callback URL: enter `http://path_to_opauth/github/oauth2callback`
   
3. Configure Opauth-GitLab strategy with `client_id` and `client_secret`.

4. Direct user to `http://path_to_opauth/github` to authenticate


Strategy configuration
----------------------

Required parameters:

```php
<?php
'GitLab' => array(
	'client_id' => 'YOUR CLIENT ID',
	'client_secret' => 'YOUR CLIENT SECRET'
)
```

Optional parameters:
`scope`, `state`

License
---------
Opauth-GitLab is MIT Licensed  
Copyright © 2016 Patrik Pekarčík (http://htsys.sk)

[1]: https://github.com/opauth/opauth