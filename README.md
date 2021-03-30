## Laravel 8 Full Auth, Perfect 👌 Application : You can use this to create your own website based on Laravel 8

#### Laravel Auth is a Complete Build of Laravel 8 with Email Registration Verification, Social Authentication, User Roles and Permissions, User Profiles, and Admin restricted user management system. Built on Bootstrap 4.
[![Build Status](https://travis-ci.org/jeremykenedy/laravel-auth.svg?branch=master)](https://travis-ci.org/jeremykenedy/laravel-auth)
[![StyleCI](https://styleci.io/repos/44714043/shield?branch=master)](https://styleci.io/repos/44714043)
[![Build Status](https://scrutinizer-ci.com/g/jeremykenedy/laravel-auth/badges/build.png?b=master)](https://scrutinizer-ci.com/g/jeremykenedy/laravel-auth/build-status/master)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/jeremykenedy/laravel-auth/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/jeremykenedy/laravel-auth/?branch=master)
[![Code Intelligence Status](https://scrutinizer-ci.com/g/jeremykenedy/laravel-auth/badges/code-intelligence.svg?b=master)](https://scrutinizer-ci.com/code-intelligence)
[![All Contributors](https://img.shields.io/badge/all_contributors-23-orange.svg?style=flat-square)](#contributors)
[![MadeWithLaravel.com shield](https://madewithlaravel.com/storage/repo-shields/1342-shield.svg)](https://madewithlaravel.com/p/laravel-auth/shield-link)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

 ### Sponsor
<table>
    <tr>
        <td>
            <img src="https://cdn.auth0.com/styleguide/components/1.0.8/media/logos/img/badge.png" alt="Auth0" width="50">
        </td>
        <td>
            If you want to quickly add secure token-based authentication to Laravel apps, feel free to check Auth0's Laravel SDK and free plan at <a href="https://auth0.com/developers?utm_source=GHsponsor&utm_medium=GHsponsor&utm_campaign=laravel-auth&utm_content=auth" target="_blank">https://auth0.com/developers</a>.
        </td>
    </tr>
</table>

#### Table of contents
- [About](#about)
- [Features](#features)
- [Installation Instructions](#installation-instructions)
    - [Build the Front End Assets with Mix](#build-the-front-end-assets-with-mix)
    - [Optionally Build Cache](#optionally-build-cache)
- [Seeds](#seeds)
    - [Seeded Roles](#seeded-roles)
    - [Seeded Permissions](#seeded-permissions)
    - [Seeded Users](#seeded-users)
    - [Themes Seed List](#themes-seed-list)
- [Routes](#routes)
- [Socialite](#socialite)
    - [Get Socialite Login API Keys](#get-socialite-login-api-keys)
    - [Add More Socialite Logins](#add-more-socialite-logins)
- [Other API keys](#other-api-keys)
- [Environment File](#environment-file)
- [Updates](#updates)
- [Screenshots](#screenshots)
- [File Tree](#file-tree)
- [Opening an Issue](#opening-an-issue)
- [Laravel Auth License](#laravel-auth-license)
- [Contributors](#Contributors)

### About
Laravel 8 with user authentication, registration with email confirmation, social media authentication, password recovery, and captcha protection. Uses official [Bootstrap 4](https://getbootstrap.com). This also makes full use of Controllers for the routes, templates for the views, and makes use of middleware for routing. Project can be stood up in minutes.

### Features
#### A [Laravel](https://laravel.com/) 8.x with [Bootstrap](https://getbootstrap.com) 4.x project.

| Laravel Auth Features  |
| :------------ |
|Built on [Laravel](https://laravel.com/) 8|
|Built on [Bootstrap](https://getbootstrap.com/) 4|
|Uses [MySQL](https://github.com/mysql) Database (can be changed)|
|Uses [Artisan](https://laravel.com/docs/master/artisan) to manage database migration, schema creations, and create/publish page controller templates|
|Dependencies are managed with [COMPOSER](https://getcomposer.org/)|
|Laravel Scaffolding **User** and **Administrator Authentication**.|
|User [Socialite Logins](https://github.com/laravel/socialite) ready to go - See API list used below|
|[Google Maps API v3](https://developers.google.com/maps/documentation/javascript/) for User Location lookup and Geocoding|
|CRUD (Create, Read, Update, Delete) Themes Management|
|CRUD (Create, Read, Update, Delete) User Management|
|Robust [Laravel Logging](https://laravel.com/docs/master/errors#logging) with admin UI using MonoLog|
|Google [reCaptcha Protection with Google API](https://developers.google.com/recaptcha/)|
|User Registration with email verification|
|Makes use of Laravel [Mix](https://laravel.com/docs/master/mix) to compile assets|
|Makes use of [Language Localization Files](https://laravel.com/docs/master/localization)|
|Active Nav states using [Laravel Requests](https://laravel.com/docs/master/requests)|
|Restrict User Email Activation Attempts|
|Capture IP to users table upon signup|
|Uses [Laravel Debugger](https://github.com/barryvdh/laravel-debugbar) for development|
|Makes use of [Password Strength Meter](https://github.com/elboletaire/password-strength-meter)|
|Makes use of [hideShowPassword](https://github.com/cloudfour/hideShowPassword)|
|User Avatar Image AJAX Upload with [Dropzone.js](https://www.dropzonejs.com/#configuration)|
|User Gravatar using [Gravatar API](https://github.com/creativeorange/gravatar)|
|User Password Reset via Email Token|
|User Login with remember password|
|User [Roles/ACL Implementation](https://github.com/jeremykenedy/laravel-roles)|
|Roles and Permissions GUI|
|Makes use of [Laravel's Soft Delete Structure](https://laravel.com/docs/master/eloquent#soft-deleting)|
|Soft Deleted Users Management System|
|Permanently Delete Soft Deleted Users|
|User Delete Account with Goodbye email|
|User Restore Deleted Account Token|
|Restore Soft Deleted Users|
|View Soft Deleted Users|
|Captures Soft Delete Date|
|Captures Soft Delete IP|
|Admin Routing Details UI|
|Admin PHP Information UI|
|Eloquent user profiles|
|User Themes|
|404 Page|
|403 Page|
|Configurable Email Notification via [Laravel-Exception-Notifier](https://github.com/jeremykenedy/laravel-exception-notifier)|
|Activity Logging using [Laravel-logger](https://github.com/jeremykenedy/laravel-logger)|
|Optional 2-step account login verfication with [Laravel 2-Step Verification](https://github.com/jeremykenedy/laravel2step)|
|Uses [Laravel PHP Info](https://github.com/jeremykenedy/laravel-phpinfo) package|
|Uses [Laravel Blocker](https://github.com/jeremykenedy/laravel-blocker) package|

### Installation Instructions
1. Run `git clone https://github.com/jeremykenedy/laravel-auth.git laravel-auth`
2. Create a MySQL database for the project
    * ```mysql -u root -p```, if using Vagrant: ```mysql -u homestead -psecret```
    * ```create database laravelAuth;```
    * ```\q```
3. From the projects root run `cp .env.example .env`
4. Configure your `.env` file
5. Run `composer update` from the projects root folder
6. From the projects root folder run:
```
php artisan vendor:publish --tag=laravelroles &&
php artisan vendor:publish --tag=laravel2step
```
7. From the projects root folder run `sudo chmod -R 755 ../laravel-auth`
8. From the projects root folder run `php artisan key:generate`
9. From the projects root folder run `php artisan migrate`
10. From the projects root folder run `composer dump-autoload`
11. From the projects root folder run `php artisan db:seed`
12. Compile the front end assets with [npm steps](#using-npm) or [yarn steps](#using-yarn).

#### Build the Front End Assets with Mix
##### Using Yarn:
1. From the projects root folder run `yarn install`
2. From the projects root folder run `yarn run dev` or `yarn run production`
  * You can watch assets with `yarn run watch`

##### Using NPM:
1. From the projects root folder run `npm install`
2. From the projects root folder run `npm run dev` or `npm run production`
  * You can watch assets with `npm run watch`

#### Optionally Build Cache
1. From the projects root folder run `php artisan config:cache`

###### And thats it with the caveat of setting up and configuring your development environment. I recommend [Laravel Homestead](https://laravel.com/docs/master/homestead)

### Seeds
##### Seeded Roles
  * Unverified - Level 0
  * User  - Level 1
  * Administrator - Level 5

##### Seeded Permissions
  * view.users
  * create.users
  * edit.users
  * delete.users

##### Seeded Users

|Email|Password|Access|
|:------------|:------------|:------------|
|user@user.com|password|User Access|
|admin@admin.com|password|Admin Access|

##### Themes Seed List
  * [ThemesTableSeeder](https://github.com/jeremykenedy/laravel-auth/blob/master/database/seeds/ThemesTableSeeder.php)
  * NOTE: A lot of themes render incorrectly on Bootstrap 4 since their core was built to override Bootstrap 4. These will be updated soon and ones that do not render correctly will be removed from the seed. In the mean time you can remove them from the seed or manaully from the UI or database.

##### Blocked Types Seed List
  * [BlockedTypeTableSeeder.php](https://github.com/jeremykenedy/laravel-auth/blob/master/database/seeds/BlockedTypeTableSeeder.php)

|Slug|Name|
|:------------|:------------|
|email|E-mail|
|ipAddress|IP Address|
|domain|Domain Name|
|user|User|
|city|City|
|state|State|
|country|Country|
|countryCode|Country Code|
|continent|Continent|
|region|Region|

##### Blocked Items Seed List
  * [BlockedItemsTableSeeder.php](https://github.com/jeremykenedy/laravel-auth/blob/master/database/seeds/BlockedItemsTableSeeder.php)

|Type|Value|Note|
|:------------|:------------|:------------|
|domain|test.com|Block all domains/emails @test.com|
|domain|test.ca|Block all domains/emails @test.ca|
|domain|fake.com|Block all domains/emails @fake.com|
|domain|example.com|Block all domains/emails @example.com|
|domain|mailinator.com|Block all domains/emails @mailinator.com|

### Routes

```bash
+--------+----------------------------------------+---------------------------------------+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------+
| Domain | Method                                 | URI                                   | Name                                          | Action                                                                                                          | Middleware                                                   |
+--------+----------------------------------------+---------------------------------------+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------+
|        | GET|HEAD                               | /                                     | welcome                                       | App\Http\Controllers\WelcomeController@welcome                                                                  | web,checkblocked                                             |
|        | GET|HEAD                               | _debugbar/assets/javascript           | debugbar.assets.js                            | Barryvdh\Debugbar\Controllers\AssetController@js                                                                | Barryvdh\Debugbar\Middleware\DebugbarEnabled,Closure         |
|        | GET|HEAD                               | _debugbar/assets/stylesheets          | debugbar.assets.css                           | Barryvdh\Debugbar\Controllers\AssetController@css                                                               | Barryvdh\Debugbar\Middleware\DebugbarEnabled,Closure         |
|        | DELETE                                 | _debugbar/cache/{key}/{tags?}         | debugbar.cache.delete                         | Barryvdh\Debugbar\Controllers\CacheController@delete                                                            | Barryvdh\Debugbar\Middleware\DebugbarEnabled,Closure         |
|        | GET|HEAD                               | _debugbar/clockwork/{id}              | debugbar.clockwork                            | Barryvdh\Debugbar\Controllers\OpenHandlerController@clockwork                                                   | Barryvdh\Debugbar\Middleware\DebugbarEnabled,Closure         |
|        | GET|HEAD                               | _debugbar/open                        | debugbar.openhandler                          | Barryvdh\Debugbar\Controllers\OpenHandlerController@handle                                                      | Barryvdh\Debugbar\Middleware\DebugbarEnabled,Closure         |
|        | GET|HEAD                               | _debugbar/telescope/{id}              | debugbar.telescope                            | Barryvdh\Debugbar\Controllers\TelescopeController@show                                                          | Barryvdh\Debugbar\Middleware\DebugbarEnabled,Closure         |
|        | GET|HEAD                               | activate                              | activate                                      | App\Http\Controllers\Auth\ActivateController@initial                                                            | web,activity,checkblocked,auth                               |
|        | GET|HEAD                               | activate/{token}                      | authenticated.activate                        | App\Http\Controllers\Auth\ActivateController@activate                                                           | web,activity,checkblocked,auth                               |
|        | GET|HEAD                               | activation                            | authenticated.activation-resend               | App\Http\Controllers\Auth\ActivateController@resend                                                             | web,activity,checkblocked,auth                               |
|        | GET|HEAD                               | activation-required                   | activation-required                           | App\Http\Controllers\Auth\ActivateController@activationRequired                                                 | web,auth,activated,activity,checkblocked                     |
|        | GET|HEAD                               | active-users                          |                                               | App\Http\Controllers\AdminDetailsController@activeUsers                                                         | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | GET|HEAD                               | activity                              | activity                                      | jeremykenedy\LaravelLogger\App\Http\Controllers\LaravelLoggerController@showAccessLog                           | web,auth,activity,role:admin                                 |
|        | DELETE                                 | activity/clear-activity               | clear-activity                                | jeremykenedy\LaravelLogger\App\Http\Controllers\LaravelLoggerController@clearActivityLog                        | web,auth,activity,role:admin                                 |
|        | GET|HEAD                               | activity/cleared                      | cleared                                       | jeremykenedy\LaravelLogger\App\Http\Controllers\LaravelLoggerController@showClearedActivityLog                  | web,auth,activity,role:admin                                 |
|        | GET|HEAD                               | activity/cleared/log/{id}             |                                               | jeremykenedy\LaravelLogger\App\Http\Controllers\LaravelLoggerController@showClearedAccessLogEntry               | web,auth,activity,role:admin                                 |
|        | DELETE                                 | activity/destroy-activity             | destroy-activity                              | jeremykenedy\LaravelLogger\App\Http\Controllers\LaravelLoggerController@destroyActivityLog                      | web,auth,activity,role:admin                                 |
|        | GET|HEAD                               | activity/log/{id}                     |                                               | jeremykenedy\LaravelLogger\App\Http\Controllers\LaravelLoggerController@showAccessLogEntry                      | web,auth,activity,role:admin                                 |
|        | POST                                   | activity/restore-log                  | restore-activity                              | jeremykenedy\LaravelLogger\App\Http\Controllers\LaravelLoggerController@restoreClearedActivityLog               | web,auth,activity,role:admin                                 |
|        | POST                                   | avatar/upload                         | avatar.upload                                 | App\Http\Controllers\ProfilesController@upload                                                                  | web,auth,activated,currentUser,activity,twostep,checkblocked |
|        | GET|HEAD                               | blocker                               | laravelblocker::blocker.index                 | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerController@index                                 | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | POST                                   | blocker                               | laravelblocker::blocker.store                 | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerController@store                                 | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | GET|HEAD                               | blocker-deleted                       | laravelblocker::blocker-deleted               | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerDeletedController@index                          | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | DELETE                                 | blocker-deleted-destroy-all           | laravelblocker::destroy-all-blocked           | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerDeletedController@destroyAllItems                | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | POST                                   | blocker-deleted-restore-all           | laravelblocker::blocker-deleted-restore-all   | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerDeletedController@restoreAllBlockedItems         | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | DELETE                                 | blocker-deleted/{id}                  | laravelblocker::blocker-item-destroy          | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerDeletedController@destroy                        | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | PUT                                    | blocker-deleted/{id}                  | laravelblocker::blocker-item-restore          | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerDeletedController@restoreBlockedItem             | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | GET|HEAD                               | blocker-deleted/{id}                  | laravelblocker::blocker-item-show-deleted     | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerDeletedController@show                           | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | GET|HEAD                               | blocker/create                        | laravelblocker::blocker.create                | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerController@create                                | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | DELETE                                 | blocker/{blocker}                     | laravelblocker::blocker.destroy               | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerController@destroy                               | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | PUT|PATCH                              | blocker/{blocker}                     | laravelblocker::blocker.update                | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerController@update                                | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | GET|HEAD                               | blocker/{blocker}                     | laravelblocker::blocker.show                  | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerController@show                                  | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | GET|HEAD                               | blocker/{blocker}/edit                | laravelblocker::blocker.edit                  | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerController@edit                                  | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | GET|HEAD                               | exceeded                              | exceeded                                      | App\Http\Controllers\Auth\ActivateController@exceeded                                                           | web,activity,checkblocked,auth                               |
|        | GET|HEAD                               | home                                  | public.home                                   | App\Http\Controllers\UserController@index                                                                       | web,auth,activated,activity,twostep,checkblocked             |
|        | GET|HEAD                               | images/profile/{id}/avatar/{image}    |                                               | App\Http\Controllers\ProfilesController@userProfileAvatar                                                       | web,auth,activated,currentUser,activity,twostep,checkblocked |
|        | POST                                   | login                                 |                                               | App\Http\Controllers\Auth\LoginController@login                                                                 | web,guest                                                    |
|        | GET|HEAD                               | login                                 | login                                         | App\Http\Controllers\Auth\LoginController@showLoginForm                                                         | web,guest                                                    |
|        | POST                                   | logout                                | logout                                        | App\Http\Controllers\Auth\LoginController@logout                                                                | web                                                          |
|        | GET|HEAD                               | logout                                | logout                                        | App\Http\Controllers\Auth\LoginController@logout                                                                | web,auth,activated,activity,checkblocked                     |
|        | GET|HEAD                               | logs                                  |                                               | Rap2hpoutre\LaravelLogViewer\LogViewerController@index                                                          | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | POST                                   | password/email                        | password.email                                | App\Http\Controllers\Auth\ForgotPasswordController@sendResetLinkEmail                                           | web,guest                                                    |
|        | GET|HEAD                               | password/reset                        | password.request                              | App\Http\Controllers\Auth\ForgotPasswordController@showLinkRequestForm                                          | web,guest                                                    |
|        | POST                                   | password/reset                        | password.update                               | App\Http\Controllers\Auth\ResetPasswordController@reset                                                         | web,guest                                                    |
|        | GET|HEAD                               | password/reset/{token}                | password.reset                                | App\Http\Controllers\Auth\ResetPasswordController@showResetForm                                                 | web,guest                                                    |
|        | GET|HEAD                               | permission-deleted/{id}               | laravelroles::permission-show-deleted         | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelpermissionsDeletedController@show                         | web,auth,role:admin                                          |
|        | DELETE                                 | permission-destroy/{id}               | laravelroles::permission-item-destroy         | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelpermissionsDeletedController@destroy                      | web,auth,role:admin                                          |
|        | PUT                                    | permission-restore/{id}               | laravelroles::permission-restore              | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelpermissionsDeletedController@restorePermission            | web,auth,role:admin                                          |
|        | POST                                   | permissions                           | laravelroles::permissions.store               | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelPermissionsController@store                               | web,auth,role:admin                                          |
|        | GET|HEAD                               | permissions                           | laravelroles::permissions.index               | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelPermissionsController@index                               | web,auth,role:admin                                          |
|        | GET|HEAD                               | permissions-deleted                   | laravelroles::permissions-deleted             | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelpermissionsDeletedController@index                        | web,auth,role:admin                                          |
|        | DELETE                                 | permissions-deleted-destroy-all       | laravelroles::destroy-all-deleted-permissions | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelpermissionsDeletedController@destroyAllDeletedPermissions | web,auth,role:admin                                          |
|        | POST                                   | permissions-deleted-restore-all       | laravelroles::permissions-deleted-restore-all | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelpermissionsDeletedController@restoreAllDeletedPermissions | web,auth,role:admin                                          |
|        | GET|HEAD                               | permissions/create                    | laravelroles::permissions.create              | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelPermissionsController@create                              | web,auth,role:admin                                          |
|        | GET|HEAD                               | permissions/{permission}              | laravelroles::permissions.show                | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelPermissionsController@show                                | web,auth,role:admin                                          |
|        | DELETE                                 | permissions/{permission}              | laravelroles::permissions.destroy             | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelPermissionsController@destroy                             | web,auth,role:admin                                          |
|        | PUT|PATCH                              | permissions/{permission}              | laravelroles::permissions.update              | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelPermissionsController@update                              | web,auth,role:admin                                          |
|        | GET|HEAD                               | permissions/{permission}/edit         | laravelroles::permissions.edit                | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelPermissionsController@edit                                | web,auth,role:admin                                          |
|        | GET|HEAD|POST|PUT|PATCH|DELETE|OPTIONS | php                                   |                                               | Illuminate\Routing\RedirectController                                                                           | web                                                          |
|        | GET|HEAD                               | phpinfo                               | laravelPhpInfo::phpinfo                       | jeremykenedy\LaravelPhpInfo\App\Http\Controllers\LaravelPhpInfoController@phpinfo                               | web,auth,activated,role:admin,activity,twostep               |
|        | GET|HEAD                               | profile/create                        | profile.create                                | App\Http\Controllers\ProfilesController@create                                                                  | web,auth,activated,currentUser,activity,twostep,checkblocked |
|        | PUT|PATCH                              | profile/{profile}                     | profile.update                                | App\Http\Controllers\ProfilesController@update                                                                  | web,auth,activated,currentUser,activity,twostep,checkblocked |
|        | GET|HEAD                               | profile/{profile}                     | profile.show                                  | App\Http\Controllers\ProfilesController@show                                                                    | web,auth,activated,currentUser,activity,twostep,checkblocked |
|        | GET|HEAD                               | profile/{profile}/edit                | profile.edit                                  | App\Http\Controllers\ProfilesController@edit                                                                    | web,auth,activated,currentUser,activity,twostep,checkblocked |
|        | GET|HEAD                               | profile/{username}                    | {username}                                    | App\Http\Controllers\ProfilesController@show                                                                    | web,auth,activated,activity,twostep,checkblocked             |
|        | DELETE                                 | profile/{username}/deleteUserAccount  | {username}                                    | App\Http\Controllers\ProfilesController@deleteUserAccount                                                       | web,auth,activated,currentUser,activity,twostep,checkblocked |
|        | PUT                                    | profile/{username}/updateUserAccount  | {username}                                    | App\Http\Controllers\ProfilesController@updateUserAccount                                                       | web,auth,activated,currentUser,activity,twostep,checkblocked |
|        | PUT                                    | profile/{username}/updateUserPassword | {username}                                    | App\Http\Controllers\ProfilesController@updateUserPassword                                                      | web,auth,activated,currentUser,activity,twostep,checkblocked |
|        | GET|HEAD                               | re-activate/{token}                   | user.reactivate                               | App\Http\Controllers\RestoreUserController@userReActivate                                                       | web,activity,checkblocked                                    |
|        | POST                                   | register                              |                                               | App\Http\Controllers\Auth\RegisterController@register                                                           | web,guest                                                    |
|        | GET|HEAD                               | register                              | register                                      | App\Http\Controllers\Auth\RegisterController@showRegistrationForm                                               | web,guest                                                    |
|        | GET|HEAD                               | role-deleted/{id}                     | laravelroles::role-show-deleted               | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesDeletedController@show                               | web,auth,role:admin                                          |
|        | DELETE                                 | role-destroy/{id}                     | laravelroles::role-item-destroy               | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesDeletedController@destroy                            | web,auth,role:admin                                          |
|        | PUT                                    | role-restore/{id}                     | laravelroles::role-restore                    | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesDeletedController@restoreRole                        | web,auth,role:admin                                          |
|        | POST                                   | roles                                 | laravelroles::roles.store                     | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesController@store                                     | web,auth,role:admin                                          |
|        | GET|HEAD                               | roles                                 | laravelroles::roles.index                     | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesController@index                                     | web,auth,role:admin                                          |
|        | GET|HEAD                               | roles-deleted                         | laravelroles::roles-deleted                   | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesDeletedController@index                              | web,auth,role:admin                                          |
|        | DELETE                                 | roles-deleted-destroy-all             | laravelroles::destroy-all-deleted-roles       | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesDeletedController@destroyAllDeletedRoles             | web,auth,role:admin                                          |
|        | POST                                   | roles-deleted-restore-all             | laravelroles::roles-deleted-restore-all       | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesDeletedController@restoreAllDeletedRoles             | web,auth,role:admin                                          |
|        | GET|HEAD                               | roles/create                          | laravelroles::roles.create                    | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesController@create                                    | web,auth,role:admin                                          |
|        | GET|HEAD                               | roles/{role}                          | laravelroles::roles.show                      | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesController@show                                      | web,auth,role:admin                                          |
|        | PUT|PATCH                              | roles/{role}                          | laravelroles::roles.update                    | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesController@update                                    | web,auth,role:admin                                          |
|        | DELETE                                 | roles/{role}                          | laravelroles::roles.destroy                   | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesController@destroy                                   | web,auth,role:admin                                          |
|        | GET|HEAD                               | roles/{role}/edit                     | laravelroles::roles.edit                      | jeremykenedy\LaravelRoles\App\Http\Controllers\LaravelRolesController@edit                                      | web,auth,role:admin                                          |
|        | GET|HEAD                               | routes                                |                                               | App\Http\Controllers\AdminDetailsController@listRoutes                                                          | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | POST                                   | search-blocked                        | laravelblocker::search-blocked                | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerController@search                                | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | POST                                   | search-blocked-deleted                | laravelblocker::search-blocked-deleted        | jeremykenedy\LaravelBlocker\App\Http\Controllers\LaravelBlockerDeletedController@search                         | web,checkblocked,auth,activated,role:admin,activity,twostep  |
|        | POST                                   | search-users                          | search-users                                  | App\Http\Controllers\UsersManagementController@search                                                           | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | GET|HEAD                               | social/handle/{provider}              | social.handle                                 | App\Http\Controllers\Auth\SocialController@getSocialHandle                                                      | web,activity,checkblocked                                    |
|        | GET|HEAD                               | social/redirect/{provider}            | social.redirect                               | App\Http\Controllers\Auth\SocialController@getSocialRedirect                                                    | web,activity,checkblocked                                    |
|        | GET|HEAD                               | terms                                 | terms                                         | App\Http\Controllers\TermsController@terms                                                                      | web,checkblocked                                             |
|        | GET|HEAD                               | themes                                | themes                                        | App\Http\Controllers\ThemesManagementController@index                                                           | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | POST                                   | themes                                | themes.store                                  | App\Http\Controllers\ThemesManagementController@store                                                           | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | GET|HEAD                               | themes/create                         | themes.create                                 | App\Http\Controllers\ThemesManagementController@create                                                          | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | DELETE                                 | themes/{theme}                        | themes.destroy                                | App\Http\Controllers\ThemesManagementController@destroy                                                         | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | PUT|PATCH                              | themes/{theme}                        | themes.update                                 | App\Http\Controllers\ThemesManagementController@update                                                          | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | GET|HEAD                               | themes/{theme}                        | themes.show                                   | App\Http\Controllers\ThemesManagementController@show                                                            | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | GET|HEAD                               | themes/{theme}/edit                   | themes.edit                                   | App\Http\Controllers\ThemesManagementController@edit                                                            | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | GET|HEAD                               | users                                 | users                                         | App\Http\Controllers\UsersManagementController@index                                                            | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | POST                                   | users                                 | users.store                                   | App\Http\Controllers\UsersManagementController@store                                                            | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | GET|HEAD                               | users/create                          | users.create                                  | App\Http\Controllers\UsersManagementController@create                                                           | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | GET|HEAD                               | users/deleted                         | deleted.index                                 | App\Http\Controllers\SoftDeletesController@index                                                                | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | GET|HEAD                               | users/deleted/{deleted}               | deleted.show                                  | App\Http\Controllers\SoftDeletesController@show                                                                 | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | DELETE                                 | users/deleted/{deleted}               | deleted.destroy                               | App\Http\Controllers\SoftDeletesController@destroy                                                              | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | PUT|PATCH                              | users/deleted/{deleted}               | deleted.update                                | App\Http\Controllers\SoftDeletesController@update                                                               | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | DELETE                                 | users/{user}                          | user.destroy                                  | App\Http\Controllers\UsersManagementController@destroy                                                          | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | PUT|PATCH                              | users/{user}                          | users.update                                  | App\Http\Controllers\UsersManagementController@update                                                           | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | GET|HEAD                               | users/{user}                          | users.show                                    | App\Http\Controllers\UsersManagementController@show                                                             | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | GET|HEAD                               | users/{user}/edit                     | users.edit                                    | App\Http\Controllers\UsersManagementController@edit                                                             | web,auth,activated,role:admin,activity,twostep,checkblocked  |
|        | GET|HEAD                               | verification/needed                   | laravel2step::verificationNeeded              | jeremykenedy\laravel2step\App\Http\Controllers\TwoStepController@showVerification                               | web,auth,Closure                                             |
|        | POST                                   | verification/resend                   | laravel2step::resend                          | jeremykenedy\laravel2step\App\Http\Controllers\TwoStepController@resend                                         | web,auth,Closure                                             |
|        | POST                                   | verification/verify                   | laravel2step::verify                          | jeremykenedy\laravel2step\App\Http\Controllers\TwoStepController@verify                                         | web,auth,Closure                                             |
+--------+----------------------------------------+---------------------------------------+-----------------------------------------------+-----------------------------------------------------------------------------------------------------------------+--------------------------------------------------------------+
```

### Socialite

#### Get Socialite Login API Keys:
* [Google Captcha API](https://www.google.com/recaptcha/admin#list)
* [Facebook API](https://developers.facebook.com/)
* [Twitter API](https://apps.twitter.com/)
* [Google &plus; API](https://console.developers.google.com/)
* [GitHub API](https://github.com/settings/applications/new)
* [YouTube API](https://developers.google.com/youtube/v3/getting-started)
* [Twitch TV API](https://www.twitch.tv/kraken/oauth2/clients/new)
* [Instagram API](https://instagram.com/developer/register/)
* [37 Signals API](https://github.com/basecamp/basecamp-classic-api)

#### Add More Socialite Logins
* See full list of providers: [https://socialiteproviders.github.io](https://socialiteproviders.github.io/#providers)
###### **Steps**:
  1. Go to [https://socialiteproviders.github.io](https://socialiteproviders.github.io/providers/twitch/) and select the provider to be added.
  2. From the projects root folder, in the terminal, run composer to get the needed package.
     * Example:

      ```
         composer require socialiteproviders/twitch
      ```

  3. From the projects root folder run ```composer update```
  4. Add the service provider to ```/config/services.php```
     * Example:

     ```
        'twitch' => [
            'client_id'   => env('TWITCH_KEY'),
            'client_secret' => env('TWITCH_SECRET'),
            'redirect'    => env('TWITCH_REDIRECT_URI'),
        ],
     ```

  5. Add the API credentials to ``` /.env  ```
     * Example:

      ```
         TWITCH_KEY=YOURKEYHERE
         TWITCH_SECRET=YOURSECRETHERE
         TWITCH_REDIRECT_URI=http://YOURWEBSITEURL.COM/social/handle/twitch
      ```

  6. Add the social media login link:
      * Example:
      In file ```/resources/views/auth/login.blade.php``` add ONE of the following:
         * Conventional HTML:
        ```
        <a href="{{ route('social.redirect', ['provider' => 'twitch']) }}" class="btn btn-lg btn-primary btn-block twitch">Twitch</a>
        ```
         * Use Laravel HTML Facade with [Laravel Collective](https://laravelcollective.com/):

        ```
        {!! HTML::link(route('social.redirect', ['provider' => 'twitch']), 'Twitch', array('class' => 'btn btn-lg btn-primary btn-block twitch')) !!}
        ```

### Other API keys
* [Google Maps API v3 Key](https://developers.google.com/maps/documentation/javascript/get-api-key#get-an-api-key)

### Environment File
Example `.env` file:

```bash

APP_NAME=Laravel
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost
APP_PROJECT_VERSION=7

LOG_CHANNEL=stack

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=

BROADCAST_DRIVER=pusher
CACHE_DRIVER=file
SESSION_DRIVER=file
SESSION_LIFETIME=120
QUEUE_DRIVER=sync

REDIS_HOST=127.0.0.1
REDIS_PASSWORD=null
REDIS_PORT=6379

MAIL_MAILER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS=null
MAIL_FROM_NAME="${APP_NAME}"

EMAIL_EXCEPTION_ENABLED=false
EMAIL_EXCEPTION_FROM="${MAIL_FROM_ADDRESS}"
EMAIL_EXCEPTION_TO='email1@gmail.com, email2@gmail.com'
EMAIL_EXCEPTION_CC=''
EMAIL_EXCEPTION_BCC=''
EMAIL_EXCEPTION_SUBJECT=''

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=

PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_APP_CLUSTER=

MIX_PUSHER_APP_KEY="${PUSHER_APP_KEY}"
MIX_PUSHER_APP_CLUSTER="${PUSHER_APP_CLUSTER}"

ACTIVATION=true
ACTIVATION_LIMIT_TIME_PERIOD=24
ACTIVATION_LIMIT_MAX_ATTEMPTS=3
NULL_IP_ADDRESS=0.0.0.0

DEBUG_BAR_ENVIRONMENT=local

USER_RESTORE_CUTOFF_DAYS=31
USER_RESTORE_ENCRYPTION_KEY=
USER_LIST_PAGINATION_SIZE=50

LARAVEL_2STEP_ENABLED=false
LARAVEL_2STEP_DATABASE_CONNECTION=mysql
LARAVEL_2STEP_DATABASE_TABLE=laravel2step
LARAVEL_2STEP_USER_MODEL=App\User
LARAVEL_2STEP_EMAIL_FROM=
LARAVEL_2STEP_EMAIL_FROM_NAME="Laravel 2 Step Verification"
LARAVEL_2STEP_EMAIL_SUBJECT='Laravel 2 Step Verification'
LARAVEL_2STEP_EXCEEDED_COUNT=3
LARAVEL_2STEP_EXCEEDED_COUNTDOWN_MINUTES=1440
LARAVEL_2STEP_VERIFIED_LIFETIME_MINUTES=360
LARAVEL_2STEP_RESET_BUFFER_IN_SECONDS=300
LARAVEL_2STEP_CSS_FILE="css/laravel2step/app.css"
LARAVEL_2STEP_APP_CSS_ENABLED=false
LARAVEL_2STEP_APP_CSS="css/app.css"
LARAVEL_2STEP_BOOTSTRAP_CSS_CDN_ENABLED=true
LARAVEL_2STEP_BOOTSTRAP_CSS_CDN="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css"

DEFAULT_GRAVATAR_SIZE=80
DEFAULT_GRAVATAR_FALLBACK=http://c1940652.r52.cf0.rackcdn.com/51ce28d0fb4f442061000000/Screen-Shot-2013-06-28-at-5.22.23-PM.png
DEFAULT_GRAVATAR_SECURE=false
DEFAULT_GRAVATAR_MAX_RATING=g
DEFAULT_GRAVATAR_FORCE_DEFAULT=false
DEFAULT_GRAVATAR_FORCE_EXTENSION=jpg

DROPZONE_JS_CDN=https://cdnjs.cloudflare.com/ajax/libs/dropzone/5.4.0/dropzone.js

LARAVEL_LOGGER_DATABASE_CONNECTION=mysql
LARAVEL_LOGGER_DATABASE_TABLE=laravel_logger_activity
LARAVEL_LOGGER_ROLES_ENABLED=true
LARAVEL_LOGGER_ROLES_MIDDLWARE=role:admin
LARAVEL_LOGGER_MIDDLEWARE_ENABLED=true
LARAVEL_LOGGER_USER_MODEL=App\Models\User
LARAVEL_LOGGER_PAGINATION_ENABLED=true
LARAVEL_LOGGER_PAGINATION_PER_PAGE=25
LARAVEL_LOGGER_DATATABLES_ENABLED=false
LARAVEL_LOGGER_DASHBOARD_MENU_ENABLED=true
LARAVEL_LOGGER_DASHBOARD_DRILLABLE=true
LARAVEL_LOGGER_LOG_RECORD_FAILURES_TO_FILE=true
LARAVEL_LOGGER_FLASH_MESSAGE_BLADE_ENABLED=false
LARAVEL_LOGGER_JQUERY_CDN_ENABLED=false
LARAVEL_LOGGER_JQUERY_CDN_URL=https://code.jquery.com/jquery-2.2.4.min.js
LARAVEL_LOGGER_BLADE_CSS_PLACEMENT_ENABLED=true
LARAVEL_LOGGER_BLADE_JS_PLACEMENT_ENABLED=true
LARAVEL_LOGGER_BOOTSTRAP_JS_CDN_ENABLED=false
LARAVEL_LOGGER_BOOTSTRAP_JS_CDN_URL=https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js
LARAVEL_LOGGER_FONT_AWESOME_CDN_ENABLED=false
LARAVEL_LOGGER_FONT_AWESOME_CDN_URL=https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css
LARAVEL_LOGGER_BOOTSTRAP_CSS_CDN_ENABLED=false
LARAVEL_LOGGER_BOOTSTRAP_CSS_CDN_URL=https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css

LARAVEL_BLOCKER_USER_MODEL=App\Models\User
LARAVEL_BLOCKER_AUTH_ENABLED=true
LARAVEL_BLOCKER_ROLES_ENABLED=true
LARAVEL_BLOCKER_FLASH_MESSAGES_ENABLED=false
LARAVEL_BLOCKER_JQUERY_CDN_ENABLED=false
LARAVEL_BLOCKER_BLADE_PLACEMENT_CSS='template_linked_css'
LARAVEL_BLOCKER_BLADE_PLACEMENT_JS='footer_scripts'
LARAVEL_BLOCKER_USE_TYPES_SEED_PUBLISHED=true
LARAVEL_BLOCKER_USE_ITEMS_SEED_PUBLISHED=true

# Roles Default Models
ROLES_DEFAULT_ROLE_MODEL=jeremykenedy\LaravelRoles\Models\Role
ROLES_DEFAULT_PERMISSION_MODEL=jeremykenedy\LaravelRoles\Models\Permission

# Roles database information
ROLES_DATABASE_CONNECTION=null

# Roles Misc Settings
ROLES_DEFAULT_SEPARATOR='.'

# Roles GUI Settings
ROLES_GUI_ENABLED=true
ROLES_GUI_AUTH_ENABLED=true
ROLES_GUI_MIDDLEWARE_ENABLED=true
ROLES_GUI_MIDDLEWARE='role:admin'
ROLES_GUI_BLADE_EXTENDED='layouts.app'
ROLES_GUI_TITLE_EXTENDED='template_title'
ROLES_GUI_LARAVEL_ROLES_ENABLED=true
ROLES_GUI_DATATABLES_JS_ENABLED=false
ROLES_GUI_FLASH_MESSAGES_ENABLED=false
ROLES_GUI_BLADE_PLACEMENT_CSS=template_linked_css
ROLES_GUI_BLADE_PLACEMENT_JS=footer_scripts

# Google Analytics - If blank it will not render, default is false
GOOGLE_ANALYTICS_ID=
#GOOGLE_ANALYTICS_ID='UA-XXXXXXXX-X'

# NOTE: YOU CAN REMOVE THE KEY CALL IN app.blade.php IF YOU GET A POP UP AND DO NOT WANT TO SETUP A KEY FOR DEV
# Google Maps API v3 Key - https://developers.google.com/maps/documentation/javascript/get-api-key#get-an-api-key
GOOGLEMAPS_API_STATUS=true
GOOGLEMAPS_API_KEY=YOURGOOGLEMAPSkeyHERE

# https://www.google.com/recaptcha/admin#list
ENABLE_RECAPTCHA=true
RE_CAP_SITE=YOURGOOGLECAPTCHAsitekeyHERE
RE_CAP_SECRET=YOURGOOGLECAPTCHAsecretHERE

# https://console.developers.google.com/ - NEED OAUTH CREDS
GOOGLE_ID=YOURGOOGLEPLUSidHERE
GOOGLE_SECRET=YOURGOOGLEPLUSsecretHERE
GOOGLE_REDIRECT=https://YOURWEBURLHERE.COM/social/handle/google

# https://developers.facebook.com/
FB_ID=YOURFACEBOOKidHERE
FB_SECRET=YOURFACEBOOKsecretHERE
FB_REDIRECT=https://YOURWEBURLHERE.COM/social/handle/facebook

# https://apps.twitter.com/
TW_ID=YOURTWITTERidHERE
TW_SECRET=YOURTWITTERkeyHERE
TW_REDIRECT=https://YOURWEBURLHERE.COM/social/handle/twitter

# https://github.com/settings/applications/new
GITHUB_ID=YOURIDHERE
GITHUB_SECRET=YOURSECRETHERE
GITHUB_URL=https://YOURWEBURLHERE.COM/social/handle/github

# https://developers.google.com/youtube/v3/getting-started
YOUTUBE_KEY=YOURKEYHERE
YOUTUBE_SECRET=YOURSECRETHERE
YOUTUBE_REDIRECT_URI=https://YOURWEBURLHERE.COM/social/handle/youtube

# https://dev.twitch.tv/docs/authentication/
TWITCH_KEY=YOURKEYHERE
TWITCH_SECRET=YOURSECRETHERE
TWITCH_REDIRECT_URI=https://YOURWEBURLHERE.COM/social/handle/twitch

# https://instagram.com/developer/register/
INSTAGRAM_KEY=YOURKEYHERE
INSTAGRAM_SECRET=YOURSECRETHERE
INSTAGRAM_REDIRECT_URI=https://YOURWEBURLHERE.COM/social/handle/instagram

# https://basecamp.com/
# https://github.com/basecamp/basecamp-classic-api
37SIGNALS_KEY=YOURKEYHERE
37SIGNALS_SECRET=YOURSECRETHERE
37SIGNALS_REDIRECT_URI=https://YOURWEBURLHERE.COM/social/handle/37signals

```

#### Laravel Developement Packages Used References
* https://laravel.com/docs/master/authentication
* https://laravel.com/docs/master/authorization
* https://laravel.com/docs/master/routing
* https://laravel.com/docs/master/migrations
* https://laravel.com/docs/master/queries
* https://laravel.com/docs/master/views
* https://laravel.com/docs/master/eloquent
* https://laravel.com/docs/master/eloquent-relationships
* https://laravel.com/docs/master/requests
* https://laravel.com/docs/master/errors

###### Updates:
* Update to Laravel 8
* Update to Laravel 7 [See changes in this PR](https://github.com/jeremykenedy/laravel-auth/pull/348/files)
* Update to Laravel 6
* Update to Laravel 5.8
* Added [Laravel Blocker Package](https://github.com/jeremykenedy/laravel-blocker)
* Added [PHP Info Package](https://github.com/jeremykenedy/laravel-phpinfo)
* Update to Bootstrap 4
* Update to Laravel 5.7
* Added optional 2-step account login verfication with [Laravel 2-Step Verification](https://github.com/jeremykenedy/laravel2step)
* Added activity logging using [Laravel-logger](https://github.com/jeremykenedy/laravel-logger)
* Added Configurable Email Notification using [Laravel-Exception-Notifier](https://github.com/jeremykenedy/laravel-exception-notifier)
* Update to Laravel 5.5
* Added User Delete with Goodbye email
* Added User Restore Deleted Account from email with secure token
* Added [Soft Deletes](https://laravel.com/docs/master/eloquent#soft-deleting) and Soft Deletes Management panel
* Added User Account Settings to Profile Edit
* Added User Change Password to Profile Edit
* Added User Delete Account to Profile Edit
* Added [Password Strength Meter](https://github.com/elboletaire/password-strength-meter)
* Added [hideShowPassword](https://github.com/cloudfour/hideShowPassword)
* Added Admin Routing Details
* Admin PHP Information
* Added Robust [Laravel Logging](https://laravel.com/docs/master/errors#logging) with admin UI using MonoLog
* Added Active Nav states using [Laravel Requests](https://laravel.com/docs/master/requests)
* Added [Laravel Debugger](https://github.com/barryvdh/laravel-debugbar) with Service Provider to manage status in `.env` file.
* Updated Capture IP not found IP address
* Added User Avatar Image AJAX Upload with [Dropzone.js](http://www.dropzonejs.com/#configuration)
* Added User Gravatar using Gravatar API
* Added Themes Management.
* Add user profiles with seeded list and global view
* Major overhaul on Laravel 5.4
* Update from Laravel 5.1 to 5.2
* Added eloquent editable user profile
* Added IP Capture
* Added Google Maps API v3 for User Location lookup
* Added Google Maps API v3 for User Location Input Geocoding
* Added Google Maps API v3 for User Location Map with Options
* Added CRUD(Create, Read, Update, Delete) User Management

### Screenshots
![Login](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/1laravel-auth2-login.jpg)
![Register](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/2laravel-auth2-register.jpg)
![Registration Confirmation](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/3laravel-auth2-account-req-activation.jpg)
![Registration Email](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/4laravel-auth2-activation-email.jpg)
![Registration Complete](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/5laravel-auth2-userhome-with-flash-success.jpg)
![Intial User Profile](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/6laravel-auth2-profile-mapless.jpg)
![Edit User Profile](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/7laravel-auth2-profile-edit.jpg)
![Find Location Using Google Maps API v3](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/8laravel-auth2-edit-profile-lookup.jpg)
![Profile Updated](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/9laravel-auth2-flash-success.jpg)
![Profile Semi-completed](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/10laravel-auth2-profile-with-map.jpg)

![Admin Panel Users List](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/11laravel-auth2-users-list.jpg)
![Admin Panel Delete User](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/12laravel-auth2-modal-delete.jpg)
![Admin Panel Flash Error](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/13laravel-auth2-flash-error.jpg)
![Admin Panel Show User](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/14laravel-auth2-show-edit.jpg)
![Admin Panel Edit User](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/15laravel-auth2-edit-user.jpg)
![Admin Panel Save Edits](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/16laravel-auth2-modal-save.jpg)
![Admin Panel Create User](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-auth/17laravel-auth-create-user.jpg)

![dashboard](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-logger/1-dashboard.jpg)
![drilldown](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-logger/2-drilldown.jpg)
![confirm-clear](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-logger/3-confirm-clear.jpg)
![log-cleared-msg](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-logger/4-log-cleared-msg.jpg)
![cleared-log](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-logger/5-cleared-log.jpg)
![confirm-restore](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-logger/5-confirm-restore.jpg)
![confirm-destroy](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-logger/6-confirm-destroy.jpg)
![success-destroy](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-logger/7-success-destroy.jpg)
![success-restored](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-logger/8-success-restored.jpg)
![cleared-drilldown](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-logger/9-cleared-drilldown.jpg)

![Verification Page](https://s3-us-west-2.amazonaws.com/github-project-images/laravel2step/1-verification-page.jpeg)
![Resent Email Modal](https://s3-us-west-2.amazonaws.com/github-project-images/laravel2step/2-verification-email-resent.jpeg)
![Lock Warning Modal](https://s3-us-west-2.amazonaws.com/github-project-images/laravel2step/3-lock-warning.jpeg)
![Locked Page](https://s3-us-west-2.amazonaws.com/github-project-images/laravel2step/4-lock-screen.jpeg)
![Verification Email](https://s3-us-west-2.amazonaws.com/github-project-images/laravel2step/5-verification-email.jpeg)

![Laravel Blocker Dashboard](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-blocker/blocker0.jpg)
![Laravel Blocker Search](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-blocker/blocker1.jpg)
![Laravel Blocker Create](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-blocker/blocker2.jpg)
![Laravel Blocker View](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-blocker/blocker3.jpg)
![Laravel Blocker Edit](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-blocker/blocker4.jpg)
![Laravel Blocker Delete Modal](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-blocker/blocker5.jpg)
![Laravel Blocker Deleted Dashboard](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-blocker/blocker6.jpg)
![Laravel Blocker Destroy Modal](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-blocker/blocker7.jpg)
![Laravel Blocker Flash Message](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-blocker/blocker8.jpg)
![Laravel Blocker Restore Modal](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-blocker/blocker9.jpg)
![Laravel Blocker Restore Flash Message](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-blocker/blocker10.jpg)

![Laravel Roles GUI Dashboard](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-1.png)
![Laravel Roles GUI Create New Role](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-2.png)
![Laravel Roles GUI Edit Role](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-3.png)
![Laravel Roles GUI Show Role](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-4.png)
![Laravel Roles GUI Delete Role](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-5.png)
![Laravel Roles GUI Success Deleted](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-6.png)
![Laravel Roles GUI Deleted Role Show](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-7.png)
![Laravel Roles GUI Restore Role](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-8.png)
![Laravel Roles GUI Delete Permission](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-9.png)
![Laravel Roles GUI Show Permission](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-10.png)
![Laravel Roles GUI Permissions Dashboard](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-11.png)
![Laravel Roles GUI Create New Permission](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-12.png)
![Laravel Roles GUI Roles Soft Deletes Dashboard](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-13.png)
![Laravel Roles GUI Permissions Soft Deletes Dashboard](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-14.png)
![Laravel Roles GUI Success Restore](https://s3-us-west-2.amazonaws.com/github-project-images/laravel-roles/screenshots/roles-gui-15.png)

### File Tree
```
laravel-auth
├── .editorconfig
├── .env
├── .env.example
├── .env.travis
├── .gitattributes
├── .github
│   ├── FUNDING.yml
│   └── ISSUE_TEMPLATE
│       ├── bug_report.md
│       ├── feature_request.md
│       └── project-questions-and-help.md
├── .gitignore
├── .phpunit.result.cache
├── .styleci.yml
├── .travis.yml
├── CODE_OF_CONDUCT.md
├── LICENSE
├── README.md
├── _config.yml
├── app
│   ├── Console
│   │   ├── Commands
│   │   │   └── DeleteExpiredActivations.php
│   │   └── Kernel.php
│   ├── Exceptions
│   │   └── Handler.php
│   ├── Http
│   │   ├── Controllers
│   │   │   ├── AdminDetailsController.php
│   │   │   ├── Auth
│   │   │   │   ├── ActivateController.php
│   │   │   │   ├── ForgotPasswordController.php
│   │   │   │   ├── LoginController.php
│   │   │   │   ├── RegisterController.php
│   │   │   │   ├── ResetPasswordController.php
│   │   │   │   └── SocialController.php
│   │   │   ├── Controller.php
│   │   │   ├── ProfilesController.php
│   │   │   ├── RestoreUserController.php
│   │   │   ├── SoftDeletesController.php
│   │   │   ├── TermsController.php
│   │   │   ├── ThemesManagementController.php
│   │   │   ├── UserController.php
│   │   │   ├── UsersManagementController.php
│   │   │   └── WelcomeController.php
│   │   ├── Kernel.php
│   │   ├── Middleware
│   │   │   ├── Authenticate.php
│   │   │   ├── CheckCurrentUser.php
│   │   │   ├── CheckForMaintenanceMode.php
│   │   │   ├── CheckIsUserActivated.php
│   │   │   ├── EncryptCookies.php
│   │   │   ├── RedirectIfAuthenticated.php
│   │   │   ├── TrimStrings.php
│   │   │   ├── TrustProxies.php
│   │   │   └── VerifyCsrfToken.php
│   │   ├── Requests
│   │   │   ├── DeleteUserAccount.php
│   │   │   ├── UpdateUserPasswordRequest.php
│   │   │   └── UpdateUserProfile.php
│   │   └── ViewComposers
│   │       └── ThemeComposer.php
│   ├── Logic
│   │   ├── Activation
│   │   │   └── ActivationRepository.php
│   │   └── Macros
│   │       └── HtmlMacros.php
│   ├── Mail
│   │   └── ExceptionOccured.php
│   ├── Models
│   │   ├── Activation.php
│   │   ├── Profile.php
│   │   ├── Social.php
│   │   ├── Theme.php
│   │   └── User.php
│   ├── Notifications
│   │   ├── SendActivationEmail.php
│   │   └── SendGoodbyeEmail.php
│   ├── Providers
│   │   ├── AppServiceProvider.php
│   │   ├── AuthServiceProvider.php
│   │   ├── BroadcastServiceProvider.php
│   │   ├── ComposerServiceProvider.php
│   │   ├── EventServiceProvider.php
│   │   ├── LocalEnvironmentServiceProvider.php
│   │   ├── MacroServiceProvider.php
│   │   └── RouteServiceProvider.php
│   └── Traits
│       ├── ActivationTrait.php
│       ├── CaptchaTrait.php
│       └── CaptureIpTrait.php
├── artisan
├── bootstrap
│   ├── app.php
│   ├── autoload.php
│   └── cache
│       ├── .gitignore
│       ├── packages.php
│       └── services.php
├── composer.json
├── composer.lock
├── config
│   ├── app.php
│   ├── auth.php
│   ├── broadcasting.php
│   ├── cache.php
│   ├── cors.php
│   ├── database.php
│   ├── debugbar.php
│   ├── exceptions.php
│   ├── filesystems.php
│   ├── gravatar.php
│   ├── hashing.php
│   ├── laravel2step.php
│   ├── laravelPhpInfo.php
│   ├── laravelblocker.php
│   ├── logging.php
│   ├── mail.php
│   ├── queue.php
│   ├── roles.php
│   ├── services.php
│   ├── session.php
│   ├── settings.php
│   ├── usersmanagement.php
│   └── view.php
├── database
│   ├── .gitignore
│   ├── factories
│   │   └── ModelFactory.php
│   ├── migrations
│   │   ├── 2014_10_12_000000_create_users_table.php
│   │   ├── 2014_10_12_100000_create_password_resets_table.php
│   │   ├── 2016_01_15_105324_create_roles_table.php
│   │   ├── 2016_01_15_114412_create_role_user_table.php
│   │   ├── 2016_01_26_115212_create_permissions_table.php
│   │   ├── 2016_01_26_115523_create_permission_role_table.php
│   │   ├── 2016_02_09_132439_create_permission_user_table.php
│   │   ├── 2017_03_09_082449_create_social_logins_table.php
│   │   ├── 2017_03_09_082526_create_activations_table.php
│   │   ├── 2017_03_20_213554_create_themes_table.php
│   │   ├── 2017_03_21_042918_create_profiles_table.php
│   │   ├── 2017_12_09_070937_create_two_step_auth_table.php
│   │   ├── 2019_02_19_032636_create_laravel_blocker_types_table.php
│   │   ├── 2019_02_19_045158_create_laravel_blocker_table.php
│   │   └── 2019_08_19_000000_create_failed_jobs_table.php
│   └── seeds
│       ├── BlockedItemsTableSeeder.php
│       ├── BlockedTypeTableSeeder.php
│       ├── ConnectRelationshipsSeeder.php
│       ├── DatabaseSeeder.php
│       ├── PermissionsTableSeeder.php
│       ├── RolesTableSeeder.php
│       ├── ThemesTableSeeder.php
│       └── UsersTableSeeder.php
├── license.svg
├── package-lock.json
├── package.json
├── phpunit.xml
├── public
│   ├── .htaccess
│   ├── css
│   │   ├── app.css
│   │   └── laravel2step
│   │       ├── app.css
│   │       └── app.min.css
│   ├── favicon.ico
│   ├── fonts
│   │   ├── fontawesome-webfont.eot
│   │   ├── fontawesome-webfont.svg
│   │   ├── fontawesome-webfont.ttf
│   │   ├── fontawesome-webfont.woff
│   │   ├── fontawesome-webfont.woff2
│   │   ├── glyphicons-halflings-regular.eot
│   │   ├── glyphicons-halflings-regular.svg
│   │   ├── glyphicons-halflings-regular.ttf
│   │   ├── glyphicons-halflings-regular.woff
│   │   └── glyphicons-halflings-regular.woff2
│   ├── images
│   │   ├── wink.png
│   │   └── wink.svg
│   ├── index.php
│   ├── js
│   │   ├── app.99230f42ad184f498ce6.js
│   │   ├── app.js
│   │   └── app.js.LICENSE.txt
│   ├── mix-manifest.json
│   ├── robots.txt
│   └── web.config
├── resources
│   ├── assets
│   │   ├── js
│   │   │   ├── app.js
│   │   │   ├── bootstrap.js
│   │   │   └── components
│   │   │       ├── ExampleComponent.vue
│   │   │       └── UsersCount.vue
│   │   ├── sass
│   │   │   ├── _avatar.scss
│   │   │   ├── _badges.scss
│   │   │   ├── _bootstrap-social.scss
│   │   │   ├── _buttons.scss
│   │   │   ├── _forms.scss
│   │   │   ├── _helpers.scss
│   │   │   ├── _hideShowPassword.scss
│   │   │   ├── _lists.scss
│   │   │   ├── _logs.scss
│   │   │   ├── _margins.scss
│   │   │   ├── _mixins.scss
│   │   │   ├── _modals.scss
│   │   │   ├── _panels.scss
│   │   │   ├── _password.scss
│   │   │   ├── _socials.scss
│   │   │   ├── _typography.scss
│   │   │   ├── _user-profile.scss
│   │   │   ├── _variables.scss
│   │   │   ├── _visibility.scss
│   │   │   ├── _wells.scss
│   │   │   └── app.scss
│   │   └── scss
│   │       └── laravel2step
│   │           ├── _animations.scss
│   │           ├── _mixins.scss
│   │           ├── _modals.scss
│   │           ├── _variables.scss
│   │           ├── _verification.scss
│   │           └── app.scss
│   ├── lang
│   │   ├── en
│   │   │   ├── auth.php
│   │   │   ├── emails.php
│   │   │   ├── forms.php
│   │   │   ├── modals.php
│   │   │   ├── pagination.php
│   │   │   ├── passwords.php
│   │   │   ├── permsandroles.php
│   │   │   ├── profile.php
│   │   │   ├── socials.php
│   │   │   ├── terms.php
│   │   │   ├── themes.php
│   │   │   ├── titles.php
│   │   │   ├── usersmanagement.php
│   │   │   └── validation.php
│   │   ├── fr
│   │   │   ├── auth.php
│   │   │   ├── emails.php
│   │   │   ├── forms.php
│   │   │   ├── modals.php
│   │   │   ├── pagination.php
│   │   │   ├── passwords.php
│   │   │   ├── permsandroles.php
│   │   │   ├── profile.php
│   │   │   ├── socials.php
│   │   │   ├── titles.php
│   │   │   ├── usersmanagement.php
│   │   │   └── validation.php
│   │   └── pt-br
│   │       ├── auth.php
│   │       ├── emails.php
│   │       ├── forms.php
│   │       ├── modals.php
│   │       ├── pagination.php
│   │       ├── passwords.php
│   │       ├── permsandroles.php
│   │       ├── profile.php
│   │       ├── socials.php
│   │       ├── themes.php
│   │       ├── titles.php
│   │       ├── usersmanagement.php
│   │       └── validation.php
│   └── views
│       ├── auth
│       │   ├── activation.blade.php
│       │   ├── exceeded.blade.php
│       │   ├── login.blade.php
│       │   ├── passwords
│       │   │   ├── email.blade.php
│       │   │   └── reset.blade.php
│       │   └── register.blade.php
│       ├── emails
│       │   └── exception.blade.php
│       ├── errors
│       │   ├── 403.blade.php
│       │   ├── 404.blade.php
│       │   ├── 500.blade.php
│       │   └── 503.blade.php
│       ├── home.blade.php
│       ├── layouts
│       │   └── app.blade.php
│       ├── modals
│       │   ├── modal-delete.blade.php
│       │   ├── modal-form.blade.php
│       │   └── modal-save.blade.php
│       ├── pages
│       │   ├── admin
│       │   │   ├── active-users.blade.php
│       │   │   ├── home.blade.php
│       │   │   └── route-details.blade.php
│       │   ├── public
│       │   │   └── terms.blade.php
│       │   ├── status.blade.php
│       │   └── user
│       │       └── home.blade.php
│       ├── panels
│       │   └── welcome-panel.blade.php
│       ├── partials
│       │   ├── errors.blade.php
│       │   ├── form-status.blade.php
│       │   ├── nav.blade.php
│       │   ├── search-users-form.blade.php
│       │   ├── socials-icons.blade.php
│       │   ├── socials.blade.php
│       │   ├── status-panel.blade.php
│       │   └── status.blade.php
│       ├── profiles
│       │   ├── edit.blade.php
│       │   └── show.blade.php
│       ├── scripts
│       │   ├── check-changed.blade.php
│       │   ├── datatables.blade.php
│       │   ├── delete-modal-script.blade.php
│       │   ├── form-modal-script.blade.php
│       │   ├── gmaps-address-lookup-api3.blade.php
│       │   ├── google-maps-geocode-and-map.blade.php
│       │   ├── save-modal-script.blade.php
│       │   ├── search-users.blade.php
│       │   ├── toggleStatus.blade.php
│       │   ├── tooltips.blade.php
│       │   └── user-avatar-dz.blade.php
│       ├── themesmanagement
│       │   ├── add-theme.blade.php
│       │   ├── edit-theme.blade.php
│       │   ├── show-theme.blade.php
│       │   └── show-themes.blade.php
│       ├── usersmanagement
│       │   ├── create-user.blade.php
│       │   ├── edit-user.blade.php
│       │   ├── show-deleted-user.blade.php
│       │   ├── show-deleted-users.blade.php
│       │   ├── show-user.blade.php
│       │   └── show-users.blade.php
│       └── welcome.blade.php
├── routes
│   ├── api.php
│   ├── channels.php
│   ├── console.php
│   └── web.php
├── server.php
└── webpack.mix.js
```
### If you have any questions, please let me know via email. tech.toolbox.project@gmail.com.[From KMH]
