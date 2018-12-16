/*global angular*/
var routerApp = angular.module('dnsHome', ['ui.router']);

routerApp.config(function($stateProvider, $urlRouterProvider) {

    $urlRouterProvider.otherwise('/home');

    $stateProvider

     .state('olb', {
        url: '/olb',
        views: {

            'menuView': { 
                templateUrl: 'olbmenu.html'
            },
             'simulatorView': { 
                templateUrl: 'olbhome.html'
            },
            'infoView': { 
                templateUrl: 'olbmenu.html'
            }
        }

    })
    .state('bmb', {
        url: '/bmb',
        views: {

            'menuView': { 
                templateUrl: 'bmbmenu.html'
            },
             'simulatorView': { 
                templateUrl: 'bmbhome.html'
            }
        }

    })
    .state('pingit', {
        url: '/pingit',
        views: {

            'menuView': { 
                templateUrl: 'pingitmenu.html'
            },
             'simulatorView': { 
                templateUrl: 'pingithome.html'
            }
        }

    })
});