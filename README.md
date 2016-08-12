# LPActionSheet

`LPActionSheet` is a clean and lightweight action sheet for your iOS app

### Installation

##### From CocoaPods

Coming soon

##### Manually

- Drag the LPActionSheet/LPActionSheet folder into your project.
- Import the file: #import "LPActionSheet.h"

### How to use LPActionSheet

You can initialize it like this (NS_DESIGNATED_INITIALIZER)
```objc
- (instancetype)initWithTitle:(NSString *)title
            cancelButtonTitle:(NSString *)cancelButtonTitle
       destructiveButtonTitle:(NSString *)destructiveButtonTitle
            otherButtonTitles:(NSArray *)otherButtonTitles
                      handler:(LPActionSheetBlock)actionSheetBlock NS_DESIGNATED_INITIALIZER;
```

You can quickly initialize it like this

```objc
+ (instancetype)actionSheetWithTitle:(NSString *)title
                   cancelButtonTitle:(NSString *)cancelButtonTitle
              destructiveButtonTitle:(NSString *)destructiveButtonTitle
                   otherButtonTitles:(NSArray *)otherButtonTitles
                             handler:(LPActionSheetBlock)actionSheetBlock;
```

Show it like this

```objc
- (void)show;
```

A final solution (recommend)

```objc
+ (void)showActionSheetWithTitle:(NSString *)title
               cancelButtonTitle:(NSString *)cancelButtonTitle
          destructiveButtonTitle:(NSString *)destructiveButtonTitle
               otherButtonTitles:(NSArray *)otherButtonTitles
                         handler:(LPActionSheetBlock)actionSheetBlock;
```

### Demo

```objc
[LPActionSheet showActionSheetWithTitle:@"This is a title, you can show some prompt here"
                      cancelButtonTitle:@"Cancel"
                 destructiveButtonTitle:@"Destructive"
                      otherButtonTitles:@[@"First choice", @"Second choice", @"Third choice"]
                                handler:^(LPActionSheet *actionSheet, NSInteger index) {
        NSLog(@"%ld", index);
}];
```

Portrait

![Portrait](https://github.com/wenxiangjiang/LPActionSheet/raw/master/LPActionSheet.png)

Landscape

![Landscape](https://github.com/wenxiangjiang/LPActionSheet/raw/master/LPActionSheet_Landscape.png)

### Hopes

- If you find bug when used, I hope you can Issues me, Thank you.
- If you find the function is not enough when used, I hope you can Issues me, Thank you.
- If you want to contribute code for `LPActionSheet`, please Pull Requests me, Thank you.

### License

`LPActionSheet` is distributed under the terms and conditions of the [MIT license](https://github.com/wenxiangjiang/LPActionSheet/blob/master/LICENSE)
