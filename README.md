#下拉菜单动态创建多个按钮
  #1：使用类方法创建多个动态按钮，并通过回调移除view和按钮
    NSArray *titleArray = @[@"按钮",@"按钮2",@"按钮3"];
    [SNDropDownMenu showInView:self.view andButtonTitle:titleArray completeHandlerBlock:^(NSInteger selectIndex, NSString *selectTitle) {
        NSLog(@"selectIndex= %ld selectTitle = %@",selectIndex,selectTitle);
        
    }];
    #2：类方法移除view和按钮
    [SNDropDownMenu removeView];