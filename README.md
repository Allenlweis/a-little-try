# NotePad
添加时间戳功能：
1.添加时间戳的位置在主页面的每个列表项中添加，即在notelist_item.xml布局文件中添加一个
<TextView  
       android:id="@android:id/text2"  
       android:layout_width="match_parent"  
       android:layout_height="wrap_content"  
       android:textAppearance="?android:attr/textAppearanceLarge"  
       android:gravity="center_vertical"  
       android:paddingLeft="5dp"  
       android:singleLine="true" /> 
2.在NoteList类的PROJECTION中添加COLUMN_NAME_MODIFICATION_DATE字段(该字段在NotePad中有说明)`
private static final String[] PROJECTION = new String[] {    
      NotePad.Notes._ID, // 0    
      NotePad.Notes.COLUMN_NAME_TITLE, // 1    
      NotePad.Notes.COLUMN_NAME_MODIFICATION_DATE,//在这里加入了修改时间的显示    
   };    

   
 3.修改适配器内容，增加dataColumns中装配到ListView的内容，所以要同时增加一个ID标识来存放该时间参数

![](https://github.com/Allenlweis/a-little-try/blob/master/images/1.png)
![](https://github.com/Allenlweis/a-little-try/blob/master/images/2.png)
![](https://github.com/Allenlweis/a-little-try/blob/master/images/3.png)
