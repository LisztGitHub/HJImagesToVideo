HJImagesToVideo
===============

Convert image array to mp4

This helper class takes an array of UIImages and will convert them to an mp4 at your desired path, size, and framerate

This is all you need!
```
[HJImagesToVideo videoFromImages:imageArray ToPath:path WithFPS:10 WithCallbackBlock:nil];
```
Example usage:

```
    NSString *path = [NSHomeDirectory() stringByAppendingPathComponent:
                      [NSString stringWithFormat:@"Documents/movie.mp4"]];
    NSArray * testImageArray = [[NSArray alloc] initWithObjects:
                                [UIImage imageNamed:@"frame1.png"],
                                [UIImage imageNamed:@"frame2.png"],
                                [UIImage imageNamed:@"frame3.png"],
                                [UIImage imageNamed:@"frame4.png"],
                                [UIImage imageNamed:@"frame5.png"],
                                [UIImage imageNamed:@"frame6.png"],
                                [UIImage imageNamed:@"frame7.png"],
                                [UIImage imageNamed:@"frame8.png"],
                                [UIImage imageNamed:@"frame9.png"], nil];
    
    NSString *path = [NSHomeDirectory() stringByAppendingPathComponent:
                      [NSString stringWithFormat:@"Documents/temp.mp4"]];
    [[NSFileManager defaultManager] removeItemAtPath:path error:NULL];
    [HJImagesToVideo videoFromImages:testImageArray ToPath:path WithFPS:10 WithCallbackBlock:^{
        NSLog(@"Success");
        
    }];
```
