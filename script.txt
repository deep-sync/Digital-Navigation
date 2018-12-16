/*global angular*/
var routerApp = angular.module('dnsHome', ['ui.router']);

routerApp.config(function($stateProvider, $urlRouterProvider) {

    $urlRouterProvider.otherwise('/home');

    $stateProvider

     .state('olb', {
        url: '/olb',
        views: {

            'menu': { 
                templateUrl: 'olbmenu.html'
            },
             'container': { 
                templateUrl: 'olblogin.html'
            }
        }

    })
});