<!--
This README describes the package. If you publish this package to pub.dev,
this README's contents appear on the landing page for your package.

For information about how to write a good package README, see the guide for
[writing package pages](https://dart.dev/guides/libraries/writing-package-pages).

For general information about developing packages, see the Dart guide for
[creating packages](https://dart.dev/guides/libraries/create-library-packages)
and the Flutter guide for
[developing packages and plugins](https://flutter.dev/developing-packages).
-->

A state builder.

## Features

A convenience widget to rebuild child widget without using Stateful Widget.

[builder] => return the child widget, which needs to refreshed

[routeName] => String value for id of parent widget.

[holder] => a specific String id for a `StateBuilder` widget. If you have more than one builder in a parent widget
and you just wanna refresh one of them, set  holder id for it.

This widget always goes with a `StateHandler` instance as a couple. `StateBuilder` just like
a widget wrapper and `StateHandler` will control how and when we need to rebuild the child widget.
It means you have to declare a `StateHandler` has same [routeName] with `StateBuilder`.

## Getting started

Run this command:
With Dart:
```
$ dart pub add flutter_state_builder
```
With Flutter:
```
$ flutter pub add flutter_state_builder
```

This will add a line like this to your package's pubspec.yaml (and run an implicit dart pub get):
```
dependencies:
    flutter_state_builder: ^1.0.0
```

Alternatively, your editor might support dart pub get or flutter pub get. Check the docs for your editor to learn more.

## Usage

```dart
StateHandler _handler = StateHandler('your_screen_widget_route_name');
StateBuilder(
    routeName: 'your_screen_widget_route_name',
    builder: () => child_widget,
    holder: 'a_builder_id',
)
```

* [StateHandler], which controls the state of a StateBuilder.
When you need to rebuild the builder, call this function
```
_handler.refresh();
```

## Additional information
Email: leonacky@gmail.com
