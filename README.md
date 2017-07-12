# iOSAutoLabel
iOS开发中,实现UILabel滚动,类似于跑马灯效果;

使用方法:

~~~
self.autoScrollLabel.frame = CGRectMake(CGRectGetMaxX(lab.frame)+5, CGRectGetMinY(lab.frame), SCREENW-CGRectGetMaxX(lab.frame)-15, 20);
[cell.contentView addSubview:self.autoScrollLabel];
~~~

~~~
- (CBAutoScrollLabel *)autoScrollLabel{
    if (!_autoScrollLabel) {
        _autoScrollLabel = [[CBAutoScrollLabel alloc]init];
        _autoScrollLabel.textColor = UIColorFromRGB(0x41210f);
        _autoScrollLabel.font = [UIFont systemFontOfSize:14];
        _autoScrollLabel.text = @"诚招zoedear竹帝儿省、市、县独家代理商!财富热线:400-900-7688";
        [_autoScrollLabel observeApplicationNotifications];
    }
    return _autoScrollLabel;
}
~~~
