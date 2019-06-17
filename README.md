# DEV_APParent_PM2_Script

This is a script for PM2. It will run Apparent's nodejs and reacts development process. After rebooting the Ubunut server PM2 will auto start nodejs and react. Simple automation for development. 

// need to use 'pm2 start npm -- start'	

``` 

module.exports = {
    apps : [{
      name        : "apparent-api",
      script      : "./server.js",
      watch       : true,
      env: {
        "NODE_ENV": "development",
      },
      env_production : {
       "NODE_ENV": "production"
      }
    },
    {
      name       : "apparent-client",
      cwd        : "./client",
      script     : "npm",
      args       : "start",
      watch       : true,
      env: {
        "NODE_ENV": "development",
      },
      env_production : {
        "NODE_ENV": "production"
      }
    }]
  }```


