# SQLiteToExcel
This is a Light weight Library to Convert SQLite Database to Excel and Convert Excel to SQLite.

## Featured In
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-SQLite%20To%20Excel-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/5221)

## Sample App
The sample app in the repository is available on Google Play:

<a href='https://play.google.com/store/apps/details?id=com.ajts.androidmads.sqlite2xlDemo&utm_source=AndroidMads&utm_campaign=AndroidMads&pcampaignid=MKT-Other-global-all-co-prtnr-py-PartBadge-Mar2515-1'><img alt='Get it on Google Play' src='https://play.google.com/intl/en_us/badges/images/generic/en_badge_web_generic.png'/></a>

## Features
1. Added Functionality to Import Excel into SQLite Database.
2. Added Functionality to Export Blob into Image.
3. Added Functionality to Export List of tables specified.
## How to Download
add the following library in your app level gradle file
```groovy
compile 'com.ajts.androidmads.SQLite2Excel:library:1.0.1'
```
## How to Use
#### The steps to use this Library
```xml
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
```
## Export SQLite to Excel
##### This line is used to save the exported file in default location.
```java
SqliteToExcel sqliteToExcel = new SqliteToExcel(this, "helloworld.db");
```
##### This line is used to save the exported file in used preferred location.
```java
SqliteToExcel sqliteToExcel = new SqliteToExcel(this, "helloworld.db", directory_path);
```
##### This code snippet is used to Export a single table in a database to Excel Sheet
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
##### This following code snippet is used to Export a list of table in a database to Excel Sheet
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
##### This code snippet is used to Export a every table in a database to Excel Sheet
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
## Import Excel into Database
The following snippet is used to initialize the library for Importing Excel
```java
ExcelToSQLite excelToSQLite = new ExcelToSQLite(getApplicationContext(), "helloworld.db");
```
##### The following code is used to Import Excel from Assets
```java
excelToSQLite.importFromAsset("assetFileName.xls", new ExcelToSQLite.ImportListener() {
	@Override
	public void onStart() {

	}

	@Override
	public void onCompleted(String dbName) {

	}

	@Override
	public void onError(Exception e) {

	}
});
```
##### The following code is used to Import Excel from user directory
```java
excelToSQLite.importFromAsset(directory_path, new ExcelToSQLite.ImportListener() {
	@Override
	public void onStart() {

	}

	@Override
	public void onCompleted(String dbName) {

	}

	@Override
	public void onError(Exception e) {

	}
});
```
## Using SQLite2XL
[Mail](mailto:mushtaqat3gb@gmail.com) me with your Google Play URL and I'll add your app to the list :)

Icon         | App          
------------ | ------------- 
<img src="https://lh3.googleusercontent.com/BlBW0j3sSNC8x_SzPIolZ6cdUIUKmM9XNN_m3eZc-ytalqjXZvSMK7fXeu6E8riOmA=w300-rw" width="48" height="48" /> | [Invoicer](https://play.google.com/store/apps/details?id=com.ajts.invoicer&hl=en) | 

Wiki
---------------------
Please visit the [wiki](https://github.com/androidmads/SQLite2XL/wiki) for a complete guide on SQLite2XL.

## License
<pre>
MIT License

Copyright (c) 2017 AndroidMad / Mushtaq M A

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated<br/>documentation files (the "Software"), to deal in the Software without restriction, including without limitation<br/>the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, <br/>and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all<br/> copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT<br/>NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. <br/>IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,<br/>WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE <br/>SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
</pre>
