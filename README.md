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
 
### 	• Text Expand to bottom

<details>
 <summary> View Code </summary>
 
```
 if using Column
 Text(
                'Experience the open mall for the first time and enjoy the scenery of the lake in the heart of The Breeze.',
                maxLines: 2,
                overflow: TextOverflow.ellipsis,            
              ),
 
  if using Row
  Expanded(
                  child: Text(
                    'Popular',
                    overflow: TextOverflow.ellipsis,              
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
 
      AppBar(
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
          width: double.infinity,
          decoration: BoxDecoration(
            borderRadius: BorderRadius.circular(10),
            color: Color(0xffF7F7F7),
          ),
          child: Focus(
            onFocusChange: (focus) {
              onSearch();
            },
            child: TextField(
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
          width: double.infinity,
          decoration: BoxDecoration(
            borderRadius: BorderRadius.circular(10),
            color: Color(0xffF7F7F7),
          ),
          child: Focus(
            onFocusChange: (focus) {
              onSearch();
            },
            child: TextField(
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
 }
```
 
</details>

###	• List Tile With Image
![image](https://user-images.githubusercontent.com/90954993/163768626-2b60707f-9901-4edf-a421-80a85705477a.png)


<details>
 <summary> View Code </summary>
 
```
Widget _buildTile() {
    return      
          Stack(
            children: [
              Container(
                margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
                child: Row(
                  children: [
                    // Image
                    ClipRRect(
                      borderRadius: BorderRadius.circular(10),
                      child: Image.network(
                        'https://images.unsplash.com/photo-1567880905822-56f8e06fe630?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8Y2FmZXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60',
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
                            'Title Name',
                            style: TextStyle(
                              fontWeight: FontWeight.w800,
                            ),
                          ),
                          SizedBox(height: 4),
                          Text(
                            'Category',
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
                                'Location',
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
                child: Container(
                  padding: EdgeInsets.fromLTRB(6, 4, 6, 4),
                  child: Row(
                    crossAxisAlignment: CrossAxisAlignment.center,
                    children: [
                      Icon(
                        Icons.star,
                        color: Colors.yellow,
                      ),
                      SizedBox(width: 4),
                      Text(
                        '5.0',
                        style: TextStyle(
                            color: Constants.redonesmile,
                            fontSize: 15,
                            fontWeight: FontWeight.bold),
                      ),
                      Text(
                        '/',
                        style: TextStyle(
                          color: Constants.redonesmile,
                          fontSize: 12,
                        ),
                      ),
                      Text(
                        '5',
                        style: TextStyle(
                          color: Constants.redonesmile,
                          fontSize: 12,
                        ),
                      ),
                    ],
                  ),
                ),
              ),
            ],
          );      
       }
```
 
</details>

<br />

## # Card

### 	• Card with shadow
![image](https://user-images.githubusercontent.com/90954993/163763265-b10530f6-518a-4318-9355-0daf3a13a7c3.png)

<details>
 <summary> View Code </summary>
 
```
Container(
          height: 139,
          margin: EdgeInsets.fromLTRB(24, 8, 24, 0),
          decoration: BoxDecoration(
            color: Colors.white,
            borderRadius: BorderRadius.circular(10),
            boxShadow: [
              BoxShadow(
                color: Colors.black12,
                spreadRadius: 1,
                blurRadius: 10,
                offset: Offset(0, 0), // changes position of shadow
              )
            ],
          ),
        ),
```
 
</details>


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
 
 ### 	• Location Map Box
![image](https://user-images.githubusercontent.com/90954993/163765088-ad53f41e-5c2b-4dae-9cd3-335539db7756.png)

<details>
 <summary> View Code </summary>
 
```
Widget _buildLocationMap() {
    return Column(
      crossAxisAlignment: CrossAxisAlignment.start,
      children: [
        // Title / See More
        Container(
          margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
          child: Text(
            'Location',
            style: TextStyle(
              fontSize: 16,
              fontWeight: FontWeight.w800,
              color: Colors.black,
            ),
          ),
        ),
        // Map Box
        Container(
          width: double.infinity,
          margin: EdgeInsets.fromLTRB(24, 8, 24, 0),
          decoration: BoxDecoration(
            color: Colors.white,
            borderRadius: BorderRadius.circular(10),
            boxShadow: [
              BoxShadow(
                color: Colors.black12,
                spreadRadius: 1,
                blurRadius: 10,
                offset: Offset(0, 0), // changes position of shadow
              )
            ],
          ),
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.start,
            children: [
              ClipRRect(
                borderRadius: BorderRadius.vertical(
                  top: Radius.circular(10),
                ),
                child: Image.network(
                  'https://media.wired.com/photos/59269cd37034dc5f91bec0f1/191:100/w_1280,c_limit/GoogleMapTA.jpg',
                  height: 115,
                  width: double.infinity,
                  fit: BoxFit.cover,
                ),
              ),
              Container(
                margin: EdgeInsets.fromLTRB(16, 12, 16, 0),
                child: Text(
                  'BSD Green Office Park',
                  overflow: TextOverflow.ellipsis,
                  style: TextStyle(
                    fontWeight: FontWeight.w800,
                    fontSize: 15,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.fromLTRB(16, 4, 16, 0),
                child: Text(
                  'Jl. BSD Green Office Park Jl. BSD Grand Boulevard, Sampora, BSD, Kabupaten Tangerang, Banten ',
                  maxLines: 2,
                  overflow: TextOverflow.ellipsis,
                  style: TextStyle(
                    fontSize: 13,
                  ),
                ),
              ),
              Container(
                margin: EdgeInsets.fromLTRB(16, 4, 16, 12),
                child: Text(
                  'See Direction',
                  style: TextStyle(
                    fontWeight: FontWeight.w800,
                    color: Constants.redonesmile,
                  ),
                ),
              ),
            ],
          ),
        ),
      ],
    );
  }
```
 
</details>
 


<br />

## # Horizontal / Vertical List

### 	• Vertical List
![image](https://user-images.githubusercontent.com/90954993/163768899-f3f5cc92-9700-43d8-bf44-4ece475520de.png)

<details>
 <summary> View Code </summary>
 
```
 Widget _buildMoreReferences() {
    return Column(
      children: [
        // TITLE / SEE MORE
        Container(
          margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
          child: Row(
            children: [
              Container(
                child: Expanded(
                  child: Text(
                    'More Places',
                    overflow: TextOverflow.ellipsis,
                    style: TextStyle(
                      fontSize: 16,
                      fontWeight: FontWeight.w800,
                    ),
                  ),
                ),
              ),
              InkWell(
                onTap: () {},
                child: Text(
                  "See more",
                  style: TextStyle(
                    fontSize: 16,
                    fontWeight: FontWeight.w800,
                    color: Constants.redTheme,
                  ),
                ),
              ),
            ],
          ),
        ),

        for (var i = 0; i < 6; i++)
          Stack(
            children: [
              Container(
                margin: EdgeInsets.fromLTRB(24, 12, 24, 12),
                child: Row(
                  children: [
                    // Image
                    ClipRRect(
                      borderRadius: BorderRadius.circular(10),
                      child: Image.network(
                        'https://images.unsplash.com/photo-1567880905822-56f8e06fe630?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8Y2FmZXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60',
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
                            'Title Name',
                            style: TextStyle(
                              fontWeight: FontWeight.w800,
                            ),
                          ),
                          SizedBox(height: 4),
                          Text(
                            'Category',
                            style: TextStyle(
                              fontWeight: FontWeight.w600,
                              color: Color(0xff828382),
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
                                'Location',
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
                child: Container(
                  padding: EdgeInsets.fromLTRB(6, 4, 6, 4),
                  child: Row(
                    crossAxisAlignment: CrossAxisAlignment.center,
                    children: [
                      Icon(
                        Icons.star,
                        color: Colors.yellow,
                      ),
                      SizedBox(width: 4),
                      Text(
                        '5.0',
                        style: TextStyle(
                            color: Constants.redonesmile,
                            fontSize: 15,
                            fontWeight: FontWeight.bold),
                      ),
                      Text(
                        '/',
                        style: TextStyle(
                          color: Constants.redonesmile,
                          fontSize: 12,
                        ),
                      ),
                      Text(
                        '5',
                        style: TextStyle(
                          color: Constants.redonesmile,
                          fontSize: 12,
                        ),
                      ),
                    ],
                  ),
                ),
              ),
            ],
          ),
      
      ],
    );
  }
```
 
</details>
 
 ### 	• Horizontal List
![image](https://user-images.githubusercontent.com/90954993/163767418-90fcbb54-d9dc-46f0-ae9c-2ba1537163fa.png)


<details>
 <summary> View Code </summary>
 
```
Widget _buildReferences() {
    return Column(
      crossAxisAlignment: CrossAxisAlignment.start,
      children: [
        // TITLE / SEE MORE
        Container(
          margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
          child: Row(
            children: [
              Container(
                child: Expanded(
                  child: Text(
                    'Popular',
                    overflow: TextOverflow.ellipsis,
                    style: TextStyle(
                      fontSize: 16,
                      fontWeight: FontWeight.w800,
                    ),
                  ),
                ),
              ),
              InkWell(
                onTap: () {},
                child: Container(
                  margin: EdgeInsets.fromLTRB(24, 0, 24, 0),
                  child: Text(
                    "See more",
                    style: TextStyle(
                      fontSize: 16,
                      fontWeight: FontWeight.w800,
                      color: Constants.redTheme,
                    ),
                  ),
                ),
              ),
            ],
          ),
        ),

        // PLACE CARD
        Container(
          child: SingleChildScrollView(
            scrollDirection: Axis.horizontal,
            child: Row(
              children: [
                SizedBox(width: 24),
                for (int i = 0; i < 4; i++)
                  Container(
                    margin: EdgeInsets.only(right: 20),
                    width: 160,
                    child: InkWell(
                      onTap: () {},
                      child: Column(
                        crossAxisAlignment: CrossAxisAlignment.start,
                        children: [
                          // Card image
                          Container(
                            margin: EdgeInsets.fromLTRB(0, 8, 0, 0),
                            height: 120,
                            decoration: BoxDecoration(
                              borderRadius: BorderRadius.circular(10),
                              image: DecorationImage(
                                image: NetworkImage(
                                  'https://images.unsplash.com/photo-1648737155328-0c0012cf2f20?ixlib=rb-1.2.1&ixid=MnwxMjA3fDF8MHxzZWFyY2h8MXx8bWFwfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
                                ),
                                fit: BoxFit.fill,
                                colorFilter: ColorFilter.mode(
                                    Colors.black.withOpacity(0.3),
                                    BlendMode.darken),
                              ),
                            ),
                          ),

                          // Card title
                          Container(
                            margin: EdgeInsets.fromLTRB(0, 8, 0, 0),
                            child: Text(
                              'Title Name',
                              style: TextStyle(
                                fontSize: 14,
                                fontWeight: FontWeight.w700,
                              ),
                              maxLines: 1,
                              overflow: TextOverflow.ellipsis,
                            ),
                          ),

                          // Card description
                          Container(
                            margin: EdgeInsets.fromLTRB(0, 4, 0, 0),
                            child: Text(
                              'Category',
                              style: TextStyle(
                                fontSize: 12,
                                fontWeight: FontWeight.w600,
                              ),
                              maxLines: 1,
                              overflow: TextOverflow.ellipsis,
                            ),
                          ),
                          //  is open
                          Container(
                            margin: EdgeInsets.fromLTRB(0, 4, 0, 0),
                            child: Row(
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
                          ),

                          // Card rating
                          Container(
                            margin: EdgeInsets.fromLTRB(0, 4, 0, 0),
                            child: Row(
                              children: [
                                Container(
                                  child: Icon(
                                    Icons.star_border_outlined,
                                    size: 16,
                                  ),
                                ),
                                SizedBox(width: 4),
                                Container(
                                  child: Text(
                                    "4.8 (423 ratings)",
                                    style: TextStyle(
                                      fontSize: 12,
                                      fontWeight: FontWeight.w400,
                                    ),
                                    maxLines: 1,
                                    overflow: TextOverflow.ellipsis,
                                  ),
                                ),
                              ],
                            ),
                          ),

                          // Card location
                          Container(
                            margin: EdgeInsets.fromLTRB(0, 4, 0, 0),
                            child: Row(
                              children: [
                                Container(
                                  child: Icon(
                                    Icons.pin_drop_outlined,
                                    size: 16,
                                  ),
                                ),
                                SizedBox(width: 4),
                                Container(
                                  child: Expanded(
                                    child: Text(
                                      'Address',
                                      style: TextStyle(
                                        fontSize: 12,
                                        fontWeight: FontWeight.w400,
                                      ),
                                      maxLines: 1,
                                      overflow: TextOverflow.ellipsis,
                                    ),
                                  ),
                                ),
                              ],
                            ),
                          ),
                        ],
                      ),
                    ),
                  ),
                SizedBox(width: 4),
              ],
            ),
          ),
        ),
      ],
    );
  }
```
 
</details>

### 	• Horizontal List Image Only
![image](https://user-images.githubusercontent.com/90954993/163762648-868efa67-9924-4d8c-ba95-1385213111d4.png)


<details>
 <summary> View Code </summary>
 
```
 Container(
            margin: EdgeInsets.fromLTRB(0, 8, 0, 0),
            child: SingleChildScrollView(
              scrollDirection: Axis.horizontal,
              child: Row(
                children: [
                  SizedBox(width: 24),
                  for (var i = 0; i < 4; i++)
                    Container(
                      margin: EdgeInsets.fromLTRB(0, 0, 12, 0),
                      child: ClipRRect(
                        borderRadius: BorderRadius.circular(10),
                        child: Image.network(
                          'https://images.unsplash.com/photo-1554118811-1e0d58224f24?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=847&q=80',
                          fit: BoxFit.cover,
                          width: 120,
                          height: 120,
                        ),
                      ),
                    ),
                  SizedBox(width: 12),
                ],
              ),
            ),
          ),
```
 
</details>



