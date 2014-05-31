Simple File Upload with Associated Object Kinvey + Angular
====

###Setup Kinvey
In the intro state, we use the resolve functionality of the router to not display the controller until the specific items
return data or the associated promise is resolved. The `$kinvey.init` funtion returns a promise; so once it is resolved the
`IntroCtrl` is called

```
$stateProvider
        .state('intro', {
            url: '/',
            templateUrl: 'intro.html',
            controller: 'IntroCtrl as intro',
            resolve: {
                authUser: function ($kinvey, $state) {
                    return $kinvey.init({
                        appKey: '',
                        appSecret: ''
                    });

                }
            }
        })
        .state('main', {
            url: '/main',
            templateUrl: 'main.html',
            controller: 'MainCtrl as main',
        });

$urlRouterProvider.otherwise("/");
```
###Initialize & Login




###Upload File

###Create Parent Object

###Save Relationship

###Retrieve Objects
