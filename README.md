# SQliteToExcel
This is a Light weight Library to Convert SQLite Database to Excel.
# Features
<ol>
<li>Added Functionality to Export SQLite Database into Excel.</li>
<li>Added Functionality to Export Single Table into Excel.</li>
<li>Added Functionality to Export List of tables specified.</li>
</ol>

# How to Download
To get a Git project into your build:

<li><b>Step 1. </b>Add it in your root build.gradle at the end of repositories:</li>

```java
<code>allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
  ```
  <li><b>Step 2. </b>Add the dependency</li>
 
 ```java
  implementation 'com.github.usamaahmadit8:SQliteToExcel:1.2'
  ```
  
  # How to Use
  
  The steps to use this Library
  
  ```java
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
```

# Export SQLite to Excel

This line is used to save the exported file in default location.

```java
SqliteToExcel sqliteToExcel = new SqliteToExcel(this, "helloworld.db");
```
This line is used to save the exported file in used preferred location.

```java
SqliteToExcel sqliteToExcel = new SqliteToExcel(this, "helloworld.db", directory_path);
```
This code snippet is used to Export a single table in a database to Excel Sheet

```java
sqliteToExcel.exportSingleTable("table1", "table1.xls", new SQLiteToExcel.ExportListener() {
     @Override
     public void onStart() {

     }
     @Override
     public void onCompleted(String filePath) {
     
     }
     @Override
     public void onError(Exception e) {

     }
});
```
This following code snippet is used to Export a list of table in a database to Excel Sheet

```java
sqliteToExcel.exportSpecificTables(tablesList, "table1.xls", new SQLiteToExcel.ExportListener() {
     @Override
     public void onStart() {

     }
     @Override
     public void onCompleted(String filePath) {
     
     }
     @Override
     public void onError(Exception e) {

     }
});
```
This code snippet is used to Export a every table in a database to Excel Sheet

```java
sqliteToExcel.exportAllTables("table1.xls", new SQLiteToExcel.ExportListener() {
     @Override
     public void onStart() {

     }
     @Override
     public void onCompleted(String filePath) {
     
     }
     @Override
     public void onError(Exception e) {

     }
});
```
