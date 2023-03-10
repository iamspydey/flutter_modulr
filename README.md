# Flutter ModulR

This is a separation of the project `Flutter Fusion` which allows you to generate `Modules` in the above mentioned project.

### Generate Module
```shell
flutter pub run modulr:generate Blog
```
This will generate all the files required for a `Module`

Generated Files:
- `BlogController.dart` controller file.
- `BlogPage.dart` view file.
- Services
    * `BlogService.dart` abstract service file.
    * `MockBlogService.dart` mockable service file for test service.
    * `AppBlogService.dart` main service file for Real API Service.

### Generate Controller
```shell
flutter pub run modulr:controller Comment --on=Blog
```
This will generate the new controller (`CommentController.dart`) inside the `Blog` Module.

Generated Files:
- `CommentController.dart` controller file.

### Generate Service
```shell
flutter pub run modulr:service Comment --on=Blog
```
If any module doesn't have services already you can generate services for the module using this command.

***Note: This will check for the services directory inside the provided module name. if it exists it wont generate any file and return void.***

Generated Files:
- Services
    * `CommentService.dart` abstract service file.
    * `MockCommentService.dart` mockable service file for test service.
    * `AppCommentService.dart` main service file for Real API Service.
