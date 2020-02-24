{:.py-4 .mt-4 #rake-deploy}
***
### 1. Building the Site ("rake deploy")

When you are all finished, go to the terminal in VS Code and click 'CTRL C' to stop your development server. Then, write 'rake deploy' and push enter. This does two things: 

1. It builds the site with the appropriate (full) links 
    - (so www.lib.uidaho.edu/digital/boxing/browse.html rather than http://127.0.0.1:4000/digital/boxing/browse.html)
2. It adds Google Analytics code based on the variable you added in the [_config.yml file](config.html). 
    - This prevents false hits on your analytics account.

If you didn't add analytics, that's fine too. It will build your site just the same as `jekyll build` does.

{% include bootstrap/alert.md color="warning" text="#### A Note on Google Analytics

We don't necessarily recommend adding Google Analytics to your website. Last year, we actually deleted analytics from our catalog due to patron privacy concerns related to Google's agrressive tracking of users online. 

We do assume, however, a large number of our eventual users might use the tool to collect web statistics (we do on our other sites). 

If you're interested in an analytics tool that doesn't track your users, we've enjoyed looking at Matomo recently. We haven't added a Matomo option but we might add that or another analytics tool in the future."  %}