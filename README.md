# PullLoadView
pull to refresh and loadMore recyclerView


# Screenshot
-------------------------
![screenshot](https://github.com/tosslife/PullLoadView/blob/master/simple.gif)



# How to use (参考MainActivity)
-------------------------

### Gradle

add in build.gradle:

```groovy

compile 'com.github.tosslife:pullloadview:1.0.2'

```
### Xml

After adding the gradle dependencies from above you can go to your xml layout and add the following code for a PullToLoadView:

```
   <com.srx.widget.PullToLoadView
             android:id="@+id/pullToLoadView"
             android:layout_width="match_parent"
             android:layout_height="match_parent"/>
```

### Java

To set some basic settings use the following java-code:

```
       //获取RecyclerView
       RecyclerView mRecyclerView = mPullToLoadView.getRecyclerView();

       //设置是否加载更多功能
       mPullToLoadView.isLoadMoreEnabled(true);

       //添加监听
       mPullToLoadView.setPullCallback(new PullCallback() {
           @Override
           public void onLoadMore() {
               //加载更多处理
           }

           @Override
           public void onRefresh() {
               //刷新处理
           }

           @Override
           public boolean isLoading() {
               //返回当前是否加载中
               return isLoading;
           }

           @Override
           public boolean hasLoadedAllItems() {
                //返回当前是否还有更多数据
               return isHasLoadedAll;
           }
       });

       //初始加载
       mPullToLoadView.initLoad();
```

### Thanks
-------------------------

- [vinaysshenoy/mugen](https://github.com/vinaysshenoy/mugen)

### LICENCE
-------------------------

  The MIT License (MIT)

  Copyright (c) 2015 sanrenx Inc.

  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in
  all copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
  THE SOFTWARE.
