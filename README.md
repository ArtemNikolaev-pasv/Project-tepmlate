Webdriver IO Template

install babel:
npm install --save-dev @babel/core @babel/cli @babel/preset-env @babel/register

create folder babel.config.js ->
module.exports = {
    presets: [
        ['@babel/preset-env', {
            targets: {
                node: 12
            }
        }]
    ]
};

wdio.conf.js -> 
 mochaOpts: {
    ui: 'bdd',
    compilers: ['js:@babel/register'],
    timeout: 60000
  },
