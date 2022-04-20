# My Flutter Widget

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
                    color: Colors.black87,
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

### 	• Common Appbar
![image](https://user-images.githubusercontent.com/90954993/163936186-271d2f33-1046-4fd7-8fab-bdfda7361d40.png)

<details>
 <summary> View Code </summary>
 
```
PreferredSizeWidget _buildAppBar() {
    return AppBar(
      iconTheme: IconThemeData(color: Colors.black87),
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
        style: TextStyle(
          fontWeight: FontWeight.w700,
          color: Colors.black,
        ),
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
      ],
    );
  }
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

### 	• Common TextButton
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

### 	• Common TextField
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

## # Modal

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

###	• Common List Tile
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
    return Container(
                    height: 140,
                    width: 348,
                    margin: EdgeInsets.fromLTRB(24, 8, 24, 0),
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
                            'Extra Large Pizza',
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
                                'Valid until April 15, 2022',
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
                                '2 Ticket Available',
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
                                'Regency City',
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
                  );
                }

```
 
</details>
 
 ### 	• Location Map Card
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
![image](https://user-images.githubusercontent.com/90954993/163769986-c25d8841-bb24-4b89-82ca-5a1f259fb698.png)


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
![image](https://user-images.githubusercontent.com/90954993/163770293-29cfe512-23dd-4325-8563-7bc3c0022a90.png)


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
                borderRadius: BorderRadius.circular(10),
                child: Container(
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
        SizedBox(height: 8),

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
                      borderRadius: BorderRadius.circular(10),
                      onTap: () {},
                      child: Column(
                        crossAxisAlignment: CrossAxisAlignment.start,
                        children: [
                          // Card image
                          Container(
                            height: 120,
                            decoration: BoxDecoration(
                              borderRadius: BorderRadius.circular(10),
                              image: DecorationImage(
                                image: NetworkImage(
                                  'https://images.unsplash.com/photo-1648737155328-0c0012cf2f20?ixlib=rb-1.2.1&ixid=MnwxMjA3fDF8MHxzZWFyY2h8MXx8bWFwfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
                                ),
                                fit: BoxFit.cover,
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
                              'Sushi Tei The Breeze',
                              style: TextStyle(
                                fontSize: 14,
                                fontWeight: FontWeight.bold,
                              ),
                              maxLines: 1,
                              overflow: TextOverflow.ellipsis,
                            ),
                          ),

                          // Card description
                          Container(
                            margin: EdgeInsets.fromLTRB(0, 4, 0, 0),
                            child: Text(
                              'Food and Beverages',
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

  Widget _buildPhotos() {
    return Column(
      children: [
        // Title / See More
        Container(
          margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
          child: Row(
            mainAxisAlignment: MainAxisAlignment.spaceBetween,
            children: [
              Text(
                'Photos',
                style: TextStyle(
                  fontSize: 16,
                  fontWeight: FontWeight.w800,
                  color: Colors.black,
                ),
              ),
              InkWell(
                borderRadius: BorderRadius.circular(10),
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
      ],
    );
  }
```
 
</details>

 <br />

## # Carousel

### 	• Common Carousel
![image](https://user-images.githubusercontent.com/90954993/163939373-9f57a0ed-5db8-4707-aeda-ed548c0e33df.png)

<details>
 <summary> View Code </summary>
 
```
int _current = 0;
  var headerCarousel = {
    'https://images.unsplash.com/photo-1579871494447-9811cf80d66c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8c3VzaGl8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60',
    'https://images.unsplash.com/photo-1611143669185-af224c5e3252?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8c3VzaGl8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60',
    'https://images.unsplash.com/photo-1553621042-f6e147245754?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8N3x8c3VzaGl8ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60',
    'https://images.unsplash.com/photo-1617196034796-73dfa7b1fd56?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTF8fHN1c2hpfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
  };
  Widget _buildCarousel() {
    return Container(
      child: Stack(
        children: [
          // Carousel Image
          CarouselSlider(
            options: CarouselOptions(
                viewportFraction: 1.0,
                autoPlay: true,
                aspectRatio: 16 / 9, // Common Aspect Ratio
                autoPlayInterval: Duration(seconds: 5),
                onPageChanged: (index, reason) {
                  setState(() {
                    _current = index;
                  });
                }),
            items: headerCarousel.map((i) {
              return Container(
                decoration: BoxDecoration(
                  image: DecorationImage(
                    image: NetworkImage(i),
                    fit: BoxFit.cover,
                  ),
                  color: Colors.white,
                ),
              );
            }).toList(),
          ),

          // Index Dot
          Positioned(
            bottom: 16,
            left: 0,
            right: 0,
            child: Row(
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                for (var i = 0; i < headerCarousel.length; i++)
                  AnimatedContainer(
                    duration: Duration(milliseconds: 200),
                    width: _current == i ? 16.0 : 8.0,
                    height: 8.0,
                    margin: EdgeInsets.fromLTRB(4, 0, 4, 0),
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(50),
                      color: _current == i
                          ? Colors.white
                          : Colors.white.withOpacity(0.7),
                    ),
                  ),
              ],
            ),
          ),
        ],
      ),
    );
  }

```
 
</details>

<br />

## # Detail

### 	• Common Detail
![image](https://user-images.githubusercontent.com/90954993/163943010-b98dd30d-e75d-4c4a-a94b-3b0b78dd2c20.png)

<details>
 <summary> View Code </summary>
 
```

  Widget _buildDetail() {
    return Container(
      margin: EdgeInsets.fromLTRB(24, 16, 24, 0),
      child: Column(
        crossAxisAlignment: CrossAxisAlignment.start,
        children: [
          // Places Name
          Container(
            child: Row(
              children: [
                Expanded(
                  child: Text(
                    'Sushi Tei The Breeze',
                    overflow: TextOverflow.ellipsis,
                    style: TextStyle(
                      fontWeight: FontWeight.w800,
                      fontSize: 18,
                    ),
                  ),
                ),
                Container(
                  margin: EdgeInsets.fromLTRB(16, 0, 16, 0),
                  child: IconButton(
                    padding: EdgeInsets.zero,
                    constraints: BoxConstraints(),
                    onPressed: () {},
                    icon: Icon(
                      Icons.bookmarks_outlined,
                      color: Colors.black87,
                    ),
                  ),
                ),
                IconButton(
                  padding: EdgeInsets.zero,
                  constraints: BoxConstraints(),
                  onPressed: () {},
                  icon: Icon(
                    Icons.near_me_outlined,
                    color: Colors.black87,
                  ),
                ),
              ],
            ),
          ),
          // Category
          Container(
            margin: EdgeInsets.fromLTRB(0, 4, 0, 0),
            child: Text(
              'Food and Beverages',
              style: TextStyle(
                fontWeight: FontWeight.w600,
                fontSize: 13,
              ),
            ),
          ),
          // Rating
          Container(
            margin: EdgeInsets.fromLTRB(0, 4, 0, 0),
            child: Row(
              children: [
                Icon(
                  Icons.star_border_outlined,
                  color: Colors.black87,
                ),
                SizedBox(width: 8),
                Text(
                  '4.8 (423 ratings)',
                  style: TextStyle(
                    fontSize: 13,
                  ),
                ),
              ],
            ),
          ),
          // Location
          Container(
            margin: EdgeInsets.fromLTRB(0, 4, 0, 0),
            child: Row(
              children: [
                Icon(
                  Icons.location_on_outlined,
                  color: Colors.black87,
                ),
                SizedBox(width: 8),
                Expanded(
                  child: Text(
                    'The Breeze BSD City',
                    style: TextStyle(
                      fontSize: 13,
                    ),
                  ),
                ),
                Text(
                  'See direction',
                  style: TextStyle(
                    fontWeight: FontWeight.w800,
                    color: Constants.redonesmile,
                    fontSize: 13,
                  ),
                ),
              ],
            ),
          ),
          // Open Time
          Container(
            margin: EdgeInsets.fromLTRB(0, 4, 0, 0),
            child: Row(
              children: [
                Icon(
                  Icons.watch_later_outlined,
                  color: Colors.black87,
                ),
                SizedBox(width: 8),
                Expanded(
                  child: Row(
                    children: [
                      Text(
                        'Open Now ',
                        style: TextStyle(
                            fontWeight: FontWeight.bold,
                            fontSize: 13,
                            color: Colors.green),
                      ),
                      Text(
                        'from ',
                        style: TextStyle(
                          fontSize: 13,
                        ),
                      ),
                      Text(
                        '10:00 - 21:00 ',
                        style: TextStyle(
                          fontWeight: FontWeight.bold,
                          fontSize: 13,
                        ),
                      ),
                    ],
                  ),
                ),
                Text(
                  'See details',
                  style: TextStyle(
                    fontWeight: FontWeight.w800,
                    color: Constants.redonesmile,
                    fontSize: 13,
                  ),
                ),
              ],
            ),
          ),
          // Phone Number
          Container(
            margin: EdgeInsets.fromLTRB(0, 4, 0, 0),
            child: Row(
              children: [
                Icon(
                  Icons.phone_outlined,
                  color: Colors.black87,
                ),
                SizedBox(width: 8),
                Expanded(
                  child: Text(
                    '021-1234567',
                    style: TextStyle(
                      fontSize: 13,
                    ),
                  ),
                ),
                Text(
                  'Make a call',
                  style: TextStyle(
                    fontWeight: FontWeight.w800,
                    color: Constants.redonesmile,
                    fontSize: 13,
                  ),
                ),
              ],
            ),
          ),
        ],
      ),
    );
  }

```
 
</details>

<br />

## # Text

### 	• See More Text
![image](https://user-images.githubusercontent.com/90954993/163947902-34f756d9-397e-4b88-8f88-f848a84aabc0.png)
 
![image](https://user-images.githubusercontent.com/90954993/163947942-6032eb29-bb6b-4e0e-b6d8-8ec4b3e11b64.png)

<details>
 <summary> View Code </summary>
 
```

class ExpandableText extends StatefulWidget {
  const ExpandableText(
    this.text, {
    Key key,
    this.trimLines = 2,
  })  : assert(text != null),
        super(key: key);

  final String text;
  final int trimLines;

  @override
  ExpandableTextState createState() => ExpandableTextState();
}

class ExpandableTextState extends State<ExpandableText> {
  bool _readMore = true;
  void _onTapLink() {
    setState(() => _readMore = !_readMore);
  }

  @override
  Widget build(BuildContext context) {
    final DefaultTextStyle defaultTextStyle = DefaultTextStyle.of(context);
    final colorClickableText = Colors.red;
    final widgetColor = Colors.black;
    TextSpan link = TextSpan(
        text: _readMore ? ". See more" : " See Less",
        style: TextStyle(
          color: colorClickableText,
          fontWeight: FontWeight.bold,
          fontSize: 13,
        ),
        recognizer: TapGestureRecognizer()..onTap = _onTapLink);
    Widget result = LayoutBuilder(
      builder: (BuildContext context, BoxConstraints constraints) {
        assert(constraints.hasBoundedWidth);
        final double maxWidth = constraints.maxWidth;
        // Create a TextSpan with data
        final text = TextSpan(
          text: widget.text,
        );
        // Layout and measure link
        TextPainter textPainter = TextPainter(
          text: link,
          textDirection: TextDirection
              .rtl, //better to pass this from master widget if ltr and rtl both supported
          maxLines: widget.trimLines,
          ellipsis: '...',
        );
        textPainter.layout(minWidth: constraints.minWidth, maxWidth: maxWidth);
        final linkSize = textPainter.size;
        // Layout and measure text
        textPainter.text = text;
        textPainter.layout(minWidth: constraints.minWidth, maxWidth: maxWidth);
        final textSize = textPainter.size;
        // Get the endIndex of data
        int endIndex;
        final pos = textPainter.getPositionForOffset(Offset(
          textSize.width - linkSize.width,
          textSize.height,
        ));
        endIndex = textPainter.getOffsetBefore(pos.offset);
        var textSpan;
        if (textPainter.didExceedMaxLines) {
          textSpan = TextSpan(
            text: _readMore ? widget.text.substring(0, endIndex) : widget.text,
            style: TextStyle(
              color: widgetColor,
            ),
            children: <TextSpan>[link],
          );
        } else {
          textSpan = TextSpan(
            text: widget.text,
          );
        }
        return RichText(
          softWrap: true,
          overflow: TextOverflow.clip,
          text: textSpan,
        );
      },
    );
    return result;
  }
}

```
 
</details>

<br />
 
 ## # Divider

### 	• Dot Line
![image](https://user-images.githubusercontent.com/90954993/163966857-e745d208-70db-42b3-a843-729f85584f26.png)

<details>
 <summary> View Code </summary>
 
```
class MySeparator extends StatelessWidget {
  final double height;
  final Color color;

  const MySeparator({this.height = 1, this.color = Colors.black});

  @override
  Widget build(BuildContext context) {
    return LayoutBuilder(
      builder: (BuildContext context, BoxConstraints constraints) {
        final boxWidth = constraints.constrainWidth();
        final dashWidth = 5.0;
        final dashHeight = height;
        final dashCount = (boxWidth / (2 * dashWidth)).floor();
        return Flex(
          children: List.generate(dashCount, (_) {
            return SizedBox(
              width: dashWidth,
              height: dashHeight,
              child: DecoratedBox(
                decoration: BoxDecoration(color: color),
              ),
            );
          }),
          mainAxisAlignment: MainAxisAlignment.spaceBetween,
          direction: Axis.horizontal,
        );
      },
    );
  }
}
```
 
</details>

<br />
 
## # Loading

### 	• Shimmer
![image](https://user-images.githubusercontent.com/90954993/163972609-25cd4374-9059-42af-ae8c-095af92715e6.png)

<details>
 <summary> View Code </summary>
 
```
Shimmer.fromColors(
        baseColor: Colors.grey[300],
        highlightColor: Colors.grey[100],
        child: Container(
          height: height * 0.22,
          margin: EdgeInsets.fromLTRB(24, 20, 24, 0),
          decoration: BoxDecoration(
            borderRadius: BorderRadius.circular(10),
            color: Colors.grey,
          ),
        ),
      );
```
 
</details>
 
<br />
 
## # Introduction / Onboarding Pages

### 	• Common Intro Pages
![image](https://user-images.githubusercontent.com/90954993/164208518-be52e69c-2ff7-4355-8ad1-9f74470f5ab5.png)

<details>
 <summary> View Code </summary>

[INTRODUCTION PAGES](https://github.com/ccprogrammer/my-widget/blob/main/Bulk%20Widget/introduction_page.dart)

</details>

<br />
 
## # Git Template Title

### 	• Git Template Widget

<details>
 <summary> View Code </summary>
 
```

```
 
</details>

<br />
