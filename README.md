# Nodejs

This repo will install Nodejs via chef.

### Chef

Chef is an automation tool to help with Infrastructure as Code. It also allows for the easy importation of other cookbook dependencies which can be accessed through GitHub without appropriate keys via a Berksfile.

### Pre-requirements
 - ChefDK version: 4.7.73
 - Chef Infra Client version: 15.7.32
 - Chef InSpec version: 4.18.51
 - Test Kitchen version: 2.3.4
 - Foodcritic version: 16.2.0
 - Cookstyle version: 5.20.0
##### Optional
 - Markdown based language editor

## Runnng tests

Make sure you are in the root directory:

#### Unit tests

```
chef exec rspec
```

#### Integration Tests:

##### Locally

If you are planning on adding to these tests, to increase efficiency, run:
```
kitchen create
kitchen converge
kitchen verify
```

You can then run `kitchen verify` after any altercations to the tests.

You can also run `kitchen test` to run integration tests.

##### AWS EC2

Create a environment variable that changes the .yml file onthe creation of the virtual machine.

```
KITCHEN_YAML=kitchen_cloud.yml kitchen test
```
