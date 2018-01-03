# grunt-openui5-deploy-abap

>Grunt plugin to facilitate deployment of openui5 application to SAP Gateway system. Based off the work done by @wolframK [here](https://www.sap.com/developer/tutorials/ci-best-practices-fiori-abap.html)

## Getting Started
This plugin requires Grunt `~0.4.5`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-openui5-deploy-abap --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-openui5-deploy-abap');
```

## The "openui5_deploy_abap" task

### Overview
In your project's Gruntfile, add a section named `openui5_deploy_abap` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  openui5_deploy_abap:{
    sbx:{
      targetDir:'target',
      appName: 'Z_APP_NAME',
      appDesc: 'Meaningful Name',
      package: 'Z_PACKAGE',
      transportDesc:' Description goes here',
      connection:{
          user: 'user',
          passwd: 'PASSWORD',
          ashost: 'SAPGGYCI',
          sysnr: '18',
          client: '250'
      }
    }
  },
});
```

### Options

#### targetDir
Type: `String`

Directory used as a work area during the build process.

#### appName
Type: `String`

Name of the BSP applicaiton on the SAP Gateway system.

#### appDesc
Type: `String`

Description of the BSP application on the SAP Gateway system.

#### package
Type: `String`

Package that contains the BSP applicaiton on the SAP Gateway system.

#### transportDesc
Type: `String`

Description for the transport that the BSP applicaiton is added to.

#### connection
Type: `Object`

Connection details for the SAP Gateway system.

#### connection.user
Type: `String`

Username of the user used to connect to the SAP Gateway

#### connection.passwd
Type: `String`

Password for the user used to connect to the SAP Gateway

#### connection.ashost
Type: `String`

Host string of the SAP Gateway system. Found on the properties of the connection in the SAP GUI.

#### connection.sysnr
Type: `String`

System number of the SAP Gateway system. Found on the properties of the connection in the SAP GUI.

#### connection.client
Type: `String`

Client of the SAP Gateway system. Found on the properties of the connection in the SAP GUI.

### Usage Examples

#### Default Options
In this example, the application would be deployed to system SAPGGYCI client 250 using user `user` under the name `Z_APP_NAME` in package `Z_PACKAGE`.

```js
grunt.initConfig({
  openui5_deploy_abap:{
    sbx:{
      targetDir:'target',
      appName: 'Z_APP_NAME',
      appDesc: 'Meaningful Name',
      package: 'Z_PACKAGE',
      transportDesc:' Description goes here',
      connection:{
          user: 'user',
          passwd: 'PASSWORD',
          ashost: 'SAPGGYCI',
          sysnr: '18',
          client: '250'
      }
    }
  },
});
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History
_(Nothing yet)_
