# My Flutter Widget

<br />

## # Git Template Title

### 	• Git Template Widget

<details>
 <summary> View Code </summary>
 
```

```
 
</details>

<br />

## # The Most Forgotten Code

### • IconButton no padding
<details>
 <summary>View Code</summary>
 
 ```
 IconButton(
                  padding: EdgeInsets.zero,
                  constraints: BoxConstraints(),
                  onPressed: () {},
                  icon: Icon(
                    Icons.close,
                    color: Color(0xffB2B2B2),
                  ),
                ),
```
 
 </details>
 
 ### 	• TextField expanding base on text written

<details>
 <summary> View Code </summary>
 
```
Container(
    child: TextField(               
              expands: false,
              maxLines: null,
            ),
         ),
```
 
</details>
 
### 	• Box Shadow

<details>
 <summary> View Code </summary>
 
```
boxShadow: [
     BoxShadow(
     color: Colors.black12,
     spreadRadius: 1,
     blurRadius: 10,
     offset: Offset(0, 0), // changes position of shadow
   )
```
</details>

<br />

## # AppBar

### 	• Normal Appbar
![image](https://user-images.githubusercontent.com/90954993/163549912-4d0426b9-fd43-4bc7-bab4-1677f357a616.png)

<details>
 <summary> View Code </summary>
 
```
AppBar(
        iconTheme: IconThemeData(color: Colors.black),
        backgroundColor: Colors.white,
        elevation: 1,
        titleSpacing: 0,
        automaticallyImplyLeading: false,
        leading: IconButton(
          padding: EdgeInsets.zero,
          constraints: BoxConstraints(),
          onPressed: () {
            Navigator.pop(context);
          },
          icon: Icon(
            Icons.chevron_left,
            size: 32,
          ),
        ),
        title: Text(
          'AppBar Title',
          style: Constants.textAppBar3,
        ),
        actions: [
          IconButton(
              padding: EdgeInsets.zero,
              constraints: BoxConstraints(),
              onPressed: () {},
              icon: Icon(Icons.search)),
          SizedBox(width: 24),
          IconButton(
              padding: EdgeInsets.zero,
              constraints: BoxConstraints(),
              onPressed: () {},
              icon: Icon(Icons.bookmarks_outlined)),
          SizedBox(width: 24),
          IconButton(
              padding: EdgeInsets.zero,
              constraints: BoxConstraints(),
              onPressed: () {},
              icon: Icon(Icons.airplane_ticket_outlined)),
          SizedBox(width: 24),
        ],
      ),
```
 
</details>

### • AppBar with TextField
![image](https://user-images.githubusercontent.com/90954993/163541408-6b88b79d-6856-48b7-9976-bd875e88201d.png)

<details>
 <summary> View Code </summary>
 
```
 
      appBar: AppBar(
        iconTheme: IconThemeData(color: Colors.black),
        backgroundColor: Colors.white,
        elevation: 0.1,
        titleSpacing: 0,
        automaticallyImplyLeading: false,
        toolbarHeight: 75,
        leading: IconButton(
          onPressed: () {
            Navigator.pop(context);
          },
          icon: Icon(
            Icons.chevron_left,
            size: 32,
          ),
        ),
        title: Container(
          padding: EdgeInsets.fromLTRB(10, 0, 10, 0),
          width: double.infinity(),
          decoration: BoxDecoration(
            borderRadius: BorderRadius.circular(10),
            color: Color(0xffF7F7F7),
          ),
          child: Focus(
            onFocusChange: (focus) {
              onSearch();
            },
            child: TextField(
              style: Constants.textAppBar3,
              decoration: InputDecoration(
                hintText: 'Search Places',
                hintStyle: TextStyle(
                  color: Color(0xffB2B2B2),
                ),
                border: InputBorder.none,
              ),
            ),
          ),
        ),
        actions: [
         IconButton(
                  onPressed: () {},
                  icon: Icon(
                    Icons.filter_list,
                  ),
                )    
          SizedBox(width: 12),
        ],
      ),
      
```
 
 </details>

<br />

## # Button

### 	• Normal TextButton
![image](https://user-images.githubusercontent.com/90954993/163549133-b8770113-b5ca-4298-a365-3341a56f851a.png)

<details>
 <summary> View Code </summary>
 
```
Container(
                height: 48,
                margin: EdgeInsets.fromLTRB(24, 24, 24, 24),
                decoration: BoxDecoration(
                  color: Colors.red,
                  borderRadius: BorderRadius.circular(10),
                ),
                child: TextButton(
                  onPressed: () {},
                  child: Text(
                    'Custom Button',
                    style: TextStyle(
                      fontWeight: FontWeight.bold,
                      color: Colors.white,
                    ),
                  ),
                ),
              ),
```
 
</details>

<br />

## # TextField

### 	• Normal TextField
![image](https://user-images.githubusercontent.com/90954993/163548481-f1ef57d1-0514-4145-95b4-f3723bbf25ce.png)

<details>
 <summary> View Code </summary>
 
```
Container(
          padding: EdgeInsets.fromLTRB(10, 0, 10, 0),
          width: double.infinity(),
          decoration: BoxDecoration(
            borderRadius: BorderRadius.circular(10),
            color: Color(0xffF7F7F7),
          ),
          child: Focus(
            onFocusChange: (focus) {
              onSearch();
            },
            child: TextField(
              style: Constants.textAppBar3,
              decoration: InputDecoration(
                hintText: 'Search Places',
                hintStyle: TextStyle(
                  color: Color(0xffB2B2B2),
                ),
                border: InputBorder.none,
              ),
            ),
          ),
        ),
```
 
</details>

<br />

## Modal

### 	• Show Modal
![image](https://user-images.githubusercontent.com/90954993/163543428-aed38586-afc4-4872-ae94-969f33cea233.png)

<details>
 <summary> View Code </summary>
 
```
void showCustomModal() {
    showModalBottomSheet(
      shape: RoundedRectangleBorder(
        borderRadius: BorderRadius.vertical(
          top: Radius.circular(25.0),
        ),
      ),
      backgroundColor: Colors.white,
      context: context,
      builder: (context) => Wrap(
        children: [
          Column(
            crossAxisAlignment: CrossAxisAlignment.center,
            mainAxisAlignment: MainAxisAlignment.start,
            children: [
              // Top Line
              Container(
                margin: EdgeInsets.fromLTRB(0, 12, 0, 0),
                width: 28,
                height: 4,
                decoration: BoxDecoration(
                  color: Color(0xffE5E5E5),
                  borderRadius: BorderRadius.circular(2),
                ),
              ),

              // Sheet Title
              Align(
                alignment: Alignment.centerLeft,
                child: Container(
                  margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
                  child: Text(
                    'Choose Language / Pilih Bahasa',
                    style: TextStyle(
                      color: Colors.black,
                      fontWeight: FontWeight.w800,
                      fontSize: 18,
                    ),
                    textAlign: TextAlign.start,
                  ),
                ),
              ),
              // Sheet Subtitle
              Container(
                margin: EdgeInsets.fromLTRB(24, 12, 24, 0),
                child: Text(
                  'Which language do you prefer? / Bahasa mana yang Anda sukai?',
                  style: TextStyle(
                    fontSize: 13,
                  ),
                  textAlign: TextAlign.start,
                ),
              ),
              // Sheet Button 1
              Container(
                margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
                width: double.infinity,
                height: 48,
                child: GestureDetector(
                  onTap: () {},        
              
                  child: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(8),
                      color: Colors.white,
                      border: Border.all(
                        color: Constants.redonesmile,
                        width: 1,
                      ),
                    ),
                    child: Center(
                      child: Text(
                        "Lanjutkan menggunakan bahasa Indonesia",
                        style: TextStyle(
                          color: Constants.redonesmile,
                          fontWeight: FontWeight.bold,
                        ),
                      ),
                    ),
                  ),
                ),
              ),
              // Sheet Button 2
              Container(
                margin: EdgeInsets.fromLTRB(24, 12, 24, 24),
                width: double.infinity,
                height: 48,
                child: GestureDetector(
                  onTap: () {}, 
                  child: Container(
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(8),
                      color: Colors.white,
                      border: Border.all(
                        color: Constants.redonesmile,
                        width: 1,
                      ),
                    ),
                    child: Center(
                      child: Text(
                        "Continue in English",
                        style: TextStyle(
                          color: Constants.redonesmile,
                          fontWeight: FontWeight.bold,
                        ),
                      ),
                    ),
                  ),
                ),
              ),
            ],
          ),
        ],
      ),
    );
  }
```
 
</details>

<br />

## # List Tile

###	• Normal List Tile
![image](https://user-images.githubusercontent.com/90954993/163539806-b83e1040-8093-4f2a-8f85-fcf1d0f95c44.png)

<details>
 <summary>View Code</summary>
 
 ```
 Widget _buildRecentSearch() {
  return Container(
            margin: EdgeInsets.fromLTRB(24, 12, 24, 0),
            child: Row(
              children: [
                Icon(
                  Icons.watch_later_outlined,
                  color: Color(0xffB2B2B2),
                ),
                SizedBox(width: 16),
                Column(
                  crossAxisAlignment: CrossAxisAlignment.start,
                  children: [
                    Text(
                      'Sushi Tei The Breeze',
                      style: TextStyle(fontWeight: FontWeight.w600),
                    ),
                    Text(
                      'Food & Beverages - The Breeze BSD City',
                      style: TextStyle(
                        fontSize: 12,
                      ),
                    ),
                  ],
                ),
                Spacer(),
                IconButton(
                  padding: EdgeInsets.zero,
                  constraints: BoxConstraints(),
                  onPressed: () {},
                  icon: Icon(
                    Icons.close,
                    color: Color(0xffB2B2B2),
                  ),
                ),
              ],
            ),
          ),
 };
```
 
</details>

###	• List Tile With Image
![image](https://user-images.githubusercontent.com/90954993/163541812-53d64dde-417d-44d9-8c9c-282319a205b0.png)

<details>
 <summary> View Code </summary>
 
```
Widget _buildSavedTile() {
    return Stack(
      children: [
        Container(
          margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
          child: Row(
            children: [
              // Image
              ClipRRect(
                borderRadius: BorderRadius.circular(10),
                child: Image.network(
                  'https://images.unsplash.com/photo-1567620905732-2d1ec7ab7445?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=480&q=80',
                  width: 84,
                  height: 84,
                  fit: BoxFit.cover,
                ),
              ),
              SizedBox(width: 12),

              // Detail
              Container(
                child: Column(
                  crossAxisAlignment: CrossAxisAlignment.start,
                  mainAxisAlignment: MainAxisAlignment.spaceBetween,
                  children: [
                    Text(
                      'Pancake honey',
                      style: TextStyle(
                        fontWeight: FontWeight.w800,
                      ),
                    ),
                    SizedBox(height: 4),
                    Text(
                      'Food and Beverages',
                      style: TextStyle(
                        fontWeight: FontWeight.w600,
                        fontSize: 12,
                      ),
                    ),
                    SizedBox(height: 4),
                    Row(
                      children: [
                        Icon(
                          Icons.watch_later_outlined,
                          size: 16,
                        ),
                        SizedBox(width: 4),
                        Text(
                          'Open Now',
                          style: TextStyle(
                            fontWeight: FontWeight.bold,
                            fontSize: 12,
                            color: Colors.green,
                          ),
                        ),
                      ],
                    ),
                    SizedBox(height: 4),
                    Row(
                      children: [
                        Icon(
                          Icons.location_on_outlined,
                          size: 16,
                        ),
                        SizedBox(width: 4),
                        Text(
                          'The Breeze BSD City',
                          style: TextStyle(
                            fontSize: 12,
                          ),
                        ),
                      ],
                    ),
                  ],
                ),
              ),
            ],
          ),
        ),
       Positioned(
          top: 24,
          right: 24,
          child: IconButton(
            onPressed: () {},
            icon: Icon(Icons.bookmarks_outlined),
          ),
        ),
      ],
    );
```
 
</details>

<br />

## # Card

### 	• Banner Card
![image](https://user-images.githubusercontent.com/90954993/163542407-07413611-17a4-49ba-8630-4309a306a9e4.png)

<details>
 <summary> View Code </summary>
 
```
Widget _buildCardBanner() {
    double height = MediaQuery.of(context).size.height;
    double width = MediaQuery.of(context).size.width;

    return GestureDetector(
      onTap: () {},
      child: Container(
        height: height * 0.18,
        width: double.infinity,
        margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
        padding: EdgeInsets.all(16),
        decoration: BoxDecoration(
          borderRadius: BorderRadius.circular(10),
          color: Colors.grey,
          image: DecorationImage(
            colorFilter: new ColorFilter.mode(
              Colors.black54,
              BlendMode.darken,
            ),
            image: new NetworkImage(
              'https://images.unsplash.com/photo-1583623025817-d180a2221d0a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTN8fHN1c2hpfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
            ),
            fit: BoxFit.cover,
          ),
        ),

        // Description
        child: Align(
          alignment: Alignment.centerLeft,
          child: Column(
            mainAxisAlignment: MainAxisAlignment.end,
            crossAxisAlignment: CrossAxisAlignment.start,
            children: [
              // Ticket Name
              Text(
                '4 Sushi Dinner',
                style: TextStyle(
                  color: Colors.white,
                  fontSize: 15,
                  fontWeight: FontWeight.w800,
                ),
              ),

              // Ticket Expired Date
              Row(
                children: [
                  Icon(
                    Icons.watch_later_outlined,
                    color: Colors.white,
                    size: 16,
                  ),
                  SizedBox(width: 8),
                  Text(
                    'Valid until ${DateFormat.yMMMMd().format(DateTime.now())}',
                    style: TextStyle(
                      color: Colors.white,
                      fontSize: 13,
                      fontWeight: FontWeight.w600,
                    ),
                  ),
                ],
              ),
              // Ticket Total
              Row(
                children: [
                  Icon(
                    Icons.theaters,
                    color: Colors.white,
                    size: 16,
                  ),
                  SizedBox(width: 8),
                  Text(
                    '${Random().nextInt(10)} Ticket Available',
                    style: TextStyle(
                      color: Colors.white,
                      fontSize: 13,
                      fontWeight: FontWeight.w600,
                    ),
                  ),
                ],
              ),

              // Ticket Location
              Row(
                children: [
                  Icon(
                    Icons.location_on_outlined,
                    color: Colors.white,
                    size: 16,
                  ),
                  SizedBox(width: 8),
                  Text(
                    'The Breeze BSD City',
                    style: TextStyle(
                      color: Colors.white,
                      fontSize: 13,
                      fontWeight: FontWeight.w600,
                    ),
                  ),
                ],
              ),
            ],
          ),
        ),
      ),
    );
  }


```
 
</details>


