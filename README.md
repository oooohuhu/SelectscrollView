# SelectscrollView
选择滚动框使用说明：
布局：
<com.asuka.android.asukaandroid.widget.pickview.LoopView
                android:id="@+id/picker_select"
                android:layout_width="match_parent"
                android:layout_height="match_parent"
                android:layout_marginLeft="1dp"
                app:textSize="@dimen/size_sup_big"
                app:lineColor="@color/transparent"
                app:centerTextColor="@color/white"
                />
代码：
 yearLoopView = (LoopView) contentView.findViewById(R.id.picker_select);

 List<String> slist=new ArrayList<>();
//slist附上值
 yearLoopView.setDataList(slist);//这就给选择框到入值了
//点击取到的值
 yearLoopView.setLoopListener(new LoopScrollListener() {
            @Override
            public void onItemSelect(int item) {
              String name=  slist.get(item);
            }
        });
