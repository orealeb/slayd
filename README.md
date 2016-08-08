slayd-api
=======

The API for SLAYD. To submit feedback, bugs or issues, please visit [slayd-api](https://github.com/orealeb/slayd/)

* [How to Use API](#use)
* [Prerequisite](#prereq)
* [How to Contribute](#contribute)
* [Build Agent](#build)
* [Production](#prod)
* [Development](#dev)
* [Local Development](#local-dev)

## <a name="use"></a> How to Use API
All HTTP requests can then be sent to **Production Server** [slayd-api.heroku.com](https://slayd-api.heroku.com) or **Development Server** [slayd-api.heroku.com](https://slayd-api.heroku.com).

#### RESTful API is used for all resources (User, xxx, xxx, xxx).

1. Example JavaScript (with jQuery) HTTP call for a User:
```
 $.ajax({
      type: "GET",
      url: "http://slayd-api.heroku.com/api/user/get", 
      data: {
          "transactionID": id
      },
      error: function() {
        alert("ERROR");
      },
      success: function(data) {
        alert(data);
      }
  }); 
```

## <a name="prereq"></a> Prerequisites

- Node.js ~4.2.X and NPM
- A Git client 


## <a name="contribute"></a> How to Contribute
#### Step 1: Clone repo and cd into repo directory:
```
git clone https://github.com/orealeb/slayd-api.git
cd slayd-api
```

#### Step 2: For developing new features and bug fixes, the master branch should be pulled, then create a new branch
```
git pull origin master
```

#### Step 3: Get on a branch!
If you are a contributor of the repo:
```
git checkout -b YOUR_BRANCH_NAME
```

#### Step 4: Install NodeJS
Ensure you have NodeJS installed, it can be done by following the instructions mentioned in the official site for [Node](http://nodejs.org/)

#### Step 5: Install all dependencies in package.json and start local server on port 3000
```
npm install 
node server.js
```
All HTTP requests can then be sent to http://localhost:3000

#### Step 6: Hack Away
Make any code changes relevant and then add them with: 

```
git add .
```

Create a commit message: 

```
git commit -m "your commit message" 
```

#### (Optional) Step 6.1: Sync your work from time to time.
```
git pull origin master
```

#### Step 7: Push

```
git push origin YOUR_BRANCH
```

* Go to https://github.com/orealeb/slayd-api and select your branch. Click the 'Pull Request' button (preferably of the development branch) and fill out the form. 
    * If you are sure of your changes, click the 'Pull Request' button for master branch and fill out the form. 

That's it!


### <a name="build"></a> Build Agent
* If any changes a pushed to the **master** branch, [Heroku](https://heroku.com) build agent automatically updates the changes to production server
* If any changes a pushed to the **development** branch, [Heroku](https://heroku.com) build agent automatically updates the changes to development server

### <a name="prod"></a> Production Server
* [slayd-api.heroku.com](http://slayd-api.heroku.com)

### <a name="dev"></a> Development Server
* [slayd-api-dev.heroku.com](http://slayd-api-dev.heroku.com)

### <a name="local-dev"></a> Local Development
* [localhost:3000](http:/localhost:3000/)

