# My Flutter Widget

## # The Most Forgotten Code

<details>
 <summary>View Widget</summary>
 
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
 
 ### • Rich Text
<details>
 <summary>View Code</summary>
 
 ```
RichText(
                                      text: TextSpan(
                                        children: [
                                          TextSpan(
                                            text:
                                                '5.0',
                                            style: TextStyle(
                                              color: Constants.redonesmile,
                                              fontSize: 15,
                                              fontWeight: FontWeight.bold,
                                            ),
                                          ),
                                          TextSpan(
                                            text: '/5',
                                            style: TextStyle(
                                              color: Constants.redonesmile,
                                              fontSize: 12,
                                            ),
                                          ),
                                        ],
                                      ),
                                    ),
```
 
 </details>
 
 ### • TextButton Padding
<details>
 <summary>View Code</summary>
 
 ```
TextButton(
                onPressed: () {},
                style: TextButton.styleFrom(
                  minimumSize: Size.zero,
                  padding: EdgeInsets.fromLTRB(10, 6, 10, 6),                                    
                ),
                child: Text(
                  '${recentSearches[i]['value']}',
                  style: TextStyle(
                    fontWeight: FontWeight.w600,
                    color: Colors.black,
                  ),
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
 or just wrap the column with expanded 
 
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
]
```
</details>
 
 ### 	• ListView invisible Top Space / Padding

<details>
 <summary> View Code </summary>
 
```
ListView(
      padding: EdgeInsets.zero,
      children: [
       widget(),
      ],
    );
```
</details>
 
 </details>






## # AppBar

<details>
  <summary>View Widget</summary>
 
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
            onFocusChange: (focus) {},
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
                ),    
          SizedBox(width: 12),
        ],
      ),
      
```
 
 </details>
 
 ### 	• Flexible AppBar
![image](https://user-images.githubusercontent.com/90954993/167287318-d357494d-7022-4a01-9c0a-6ef70d1602f5.png)

<details>
 <summary> View Code </summary>
 
```

    PreferredSizeWidget header() {
      return AppBar(
        backgroundColor: backgroundColor1,
        automaticallyImplyLeading: false,
        elevation: 0,
        flexibleSpace: SafeArea(
          child: Container(
            padding: EdgeInsets.all(defaultMargin),
            child: Row(
              children: [
                Image.asset(
                  'assets/images/image_profile.png',
                  width: 64,
                ),
                SizedBox(width: 12),
                Expanded(
                  child: Column(
                    crossAxisAlignment: CrossAxisAlignment.start,
                    children: [
                      Text(
                        'Hallo, Lubi ',
                        style: primaryTextStyle.copyWith(
                          fontWeight: semiBold,
                          fontSize: 24,
                        ),
                        overflow: TextOverflow.ellipsis,
                      ),
                      Text(
                        '@lubiancaaa',
                        style: subtitleTextStyle.copyWith(
                          fontSize: 16,
                        ),
                      ),
                    ],
                  ),
                ),
                SizedBox(width: 15),
                GestureDetector(
                  onTap: () {
                    Navigator.pushNamedAndRemoveUntil(
                        context, '/sign-in', (route) => false);
                  },
                  child: Image.asset(
                    'assets/images/button_exit.png',
                    width: 20,
                  ),
                ),
              ],
            ),
          ),
        ),
      );
    }

```
 
</details>
 
</details>



## # Button

<details>
  <summary>View Widget</summary>
 
### 	• Common TextButton
![image](https://user-images.githubusercontent.com/90954993/163549133-b8770113-b5ca-4298-a365-3341a56f851a.png)

<details>
 <summary> View Code </summary>
 
```
Container(
                height: 48,
                margin: EdgeInsets.fromLTRB(24, 24, 24, 24),      
                child: TextButton(
                  onPressed: () {},
                style: TextButton.styleFrom(
                      backgroundColor: Colors.red,
                      // minimumSize:Size.zero,
                      // padding: EdgeInsets.zero,
                      // side: BorderSide(
                      //   color: Colors.red,
                      // ),
            shape: RoundedRectangleBorder(
              borderRadius: BorderRadius.circular(10),
            ),
          ),
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
 
 </details>



## # TextField

<details>
  <summary>View Widget</summary>

### 	• Common TextField
![image](https://user-images.githubusercontent.com/90954993/163548481-f1ef57d1-0514-4145-95b4-f3723bbf25ce.png)

<details>
 <summary> View Code </summary>
 
```
Container(
                    margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
                    padding: EdgeInsets.fromLTRB(16, 4, 16, 4),
                    width: double.infinity,
                    // height: MediaQuery.of(context).size.height * 0.065,
                    decoration: BoxDecoration(
                      borderRadius: BorderRadius.circular(10),
                      color: Color(0xffF7F7F7),
                    ),
                    child: Center(
                      child: Focus(
                        onFocusChange: (focus) {},
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
                  ),
```
 
</details>

### 	• Common Textfield 2
![image](https://user-images.githubusercontent.com/90954993/164273703-ede4be0d-2542-4b8b-b3d3-4acc0cb0913f.png)

<details>
 <summary> View Code </summary>
 
```
Container(
              margin: EdgeInsets.fromLTRB(24, 26, 24, 0),
              child: TextField(
                textAlign: TextAlign.center,
                style: TextStyle(
                  color: Colors.white.withOpacity(0.87),
                  fontSize: 22,
                ),
                decoration: InputDecoration(
                  hintText: 'Please enter your name here',
                  hintStyle: TextStyle(
                    color: Colors.white.withOpacity(0.67),
                    fontSize: 16,
                  ),
                  border: InputBorder.none,
                ),
              ),
            ),
```
 
</details>
 
 </details>
 


## # Modal

<details>
  <summary>View Widget</summary>
 
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

</details>
 


## # List Tile

 <details>
  <summary>View Widget</summary>
  
###	• Common List Tile
![image](https://user-images.githubusercontent.com/90954993/164884412-177558f0-a8e5-40b1-ba3e-2d19f3527107.png)

<details>
 <summary>View Code</summary>
 
 ```
 Widget _buildRecentSearch() {
  return    
          InkWell(
            onTap: () {},
            child: Stack(
              children: [
                Container(
                  margin: EdgeInsets.fromLTRB(24, 12, 24, 12),
                  child: Row(
                    children: [
                      // Image
                      ClipRRect(
                        borderRadius: BorderRadius.circular(10),
                        child: Image.network(
                          'https://images.unsplash.com/photo-1549877452-9c387954fbc2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8cGxhY2VzfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
                          width: 84,
                          height: 84,
                          fit: BoxFit.cover,
                        ),
                      ),
                      SizedBox(width: 12),

                      // Detail
                      Expanded( 
                          child: Column(
                            crossAxisAlignment: CrossAxisAlignment.start,
                            mainAxisAlignment: MainAxisAlignment.spaceBetween,
                            children: [
                              // nama
                              Text(
                                'Store Name',
                                style: TextStyle(
                                  fontWeight: FontWeight.w800,
                                ),
                              ),
                              SizedBox(height: 4),

                              // kategori
                              Text(
                                'Category',
                                style: TextStyle(
                                  fontWeight: FontWeight.w600,
                                  fontSize: 12,
                                ),
                              ),
                              SizedBox(height: 4),

                              // status buka
                              Row(
                                children: [
                                  Icon(
                                    Icons.watch_later_outlined,
                                    size: 16,
                                  ),
                                  SizedBox(width: 4),
                                  Text(
                                    'Open Status',
                                    style: TextStyle(
                                      fontWeight: FontWeight.bold,
                                      fontSize: 12,
                                      color: Colors.green,
                                    ),
                                  ),
                                ],
                              ),
                              SizedBox(height: 4),

                              // alamat
                              Row(
                                children: [
                                  Icon(
                                    Icons.location_on_outlined,
                                    size: 16,
                                  ),
                                  SizedBox(width: 4),
                                  Expanded(
                                    child: Text(
                                      'Location',
                                      maxLines: 1,
                                      style: TextStyle(
                                        fontSize: 12,
                                      ),
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
                         RichText(
                          text: TextSpan(
                            children: [
                              TextSpan(
                                text: '5.0',
                                style: TextStyle(
                                  color: Colors.black,
                                  fontSize: 15,
                                  fontWeight: FontWeight.bold,
                                ),
                              ),
                              TextSpan(
                                text: '/5',
                                style: TextStyle(
                                  color: Colors.black,
                                  fontSize: 12,
                                ),
                              ),
                            ],
                          ),
                        ),
                      ],
                    ),
                  ),
                ),
              ],
            ),
          );
 }
```
 
</details>

 </details>
 


## # Card

<details>
  <summary>View Widget</summary>
 
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
 
 ### 	• Card with stretch header image, [StackOverflow](https://stackoverflow.com/questions/54885879/flutter-how-to-handle-image-with-fixed-size-inside-box)
![image](https://user-images.githubusercontent.com/90954993/167739655-9d511126-db40-4976-b4d5-26e68555e40d.png)

<details>
 <summary> View Code </summary>
 
```
Column(
                crossAxisAlignment: CrossAxisAlignment.stretch,  // add this
                children: <Widget>[
                  ClipRRect(
                    borderRadius: BorderRadius.only(
                      topLeft: Radius.circular(8.0),
                      topRight: Radius.circular(8.0),
                    ),
                    child: Image.network(
                        'https://placeimg.com/640/480/any',
                       // width: 300,
                        height: 150,
                        fit:BoxFit.fill

                    ),
                  ),
                  ListTile(
                    title: Text('Pub 1'),
                    subtitle: Text('Location 1'),
                  ),
                ],
              ),
```
 
</details>

### 	• Review Card
![image](https://user-images.githubusercontent.com/90954993/165220946-6c16fbc2-6f51-45fb-9e89-5b7720927bed.png)

<details>
 <summary> View Code </summary>
 
```

  Widget _buildReviews() {
    return Container(
      width: 348,
      margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
      padding: EdgeInsets.all(16),
      decoration: BoxDecoration(
        borderRadius: BorderRadius.circular(10),
        border: Border.all(
          color: Color(0xffD9D9D9),
          width: 1,
        ),
      ),
      // Description
      child: Column(
        children: [
          // Review Card Header
          Row(
            children: [
              ClipRRect(
                borderRadius: BorderRadius.circular(50),
                child: Image.network(
                  'https://images.unsplash.com/photo-1539571696357-5a69c17a67c6?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8N3x8cGVvcGxlfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
                  width: 42,
                  height: 42,
                  fit: BoxFit.cover,
                ),
              ),
              SizedBox(width: 12),
              Column(
                crossAxisAlignment: CrossAxisAlignment.start,
                children: [
                  Text(
                    'Jeanice Ang',
                    style: TextStyle(
                      fontWeight: FontWeight.w800,
                    ),
                  ),
                  Text(
                    'Jeanice Ang',
                    style: TextStyle(
                      color: Color(0xff828382),
                      fontSize: 11,
                    ),
                  ),
                ],
              ),
              Spacer(),

              // Rating
              Container(
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
            ],
          ),

          Container(
            margin: EdgeInsets.fromLTRB(0, 12, 0, 12),
        //    child: MySeparator(
        //      height: 1,
        //      color: Color(0xffD9D9D9),
            ),
          ),

          Container(
            child: Text(
              'Sushi tasted really good with a lot of varieties to choose from. Would recommend this restaurant to anyone searching for the best sushi in the town.Sushi tasted really good with a lot of varieties to choose from. Would recommend this restaurant to anyone searching for the best sushi in the town.',
              maxLines: 3,
              overflow: TextOverflow.ellipsis,
              style: TextStyle(
                fontSize: 13,
              ),
            ),
          )
        ],
      ),
    );
  }

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
      decoration: BoxDecoration(
        borderRadius: BorderRadius.circular(10),
        color: Colors.grey,
        image: DecorationImage(
          colorFilter: ColorFilter.mode(
            Colors.black54,
            BlendMode.darken,
          ),
          image: NetworkImage(
            'https://images.unsplash.com/photo-1583623025817-d180a2221d0a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MTN8fHN1c2hpfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
          ),
          fit: BoxFit.cover,
        ),
      ),
      // Description
      child: Material(
        color: Colors.transparent,
        child: InkWell(
          borderRadius: BorderRadius.circular(10),
          onTap: () {},
          child: Align(
            alignment: Alignment.centerLeft,
            child: Padding(
              padding: EdgeInsets.all(16.0),
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
          ),
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
 
</details>





## # Horizontal / Vertical List

<details>
  <summary>View Widget</summary>
 
### 	• Vertical List
![image](https://user-images.githubusercontent.com/90954993/164884385-997fabb8-758a-48d6-8eaa-20f40b7ec34e.png)


<details>
 <summary> View Code </summary>
 
```
  Widget _buildMoreReferences() {
    return Column(children: [
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
                  color: Colors.blue,
                ),
              ),
            ),
          ],
        ),
      ),

      for (var i = 0; i < 5; i++)
        InkWell(
          onTap: () {},
          child: Stack(
            children: [
              Container(
                margin: EdgeInsets.fromLTRB(24, 12, 24, 12),
                child: Row(
                  children: [
                    // Image
                    ClipRRect(
                      borderRadius: BorderRadius.circular(10),
                      child: Image.network(
                        'https://images.unsplash.com/photo-1549877452-9c387954fbc2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8cGxhY2VzfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60',
                        width: 84,
                        height: 84,
                        fit: BoxFit.cover,
                      ),
                    ),
                    SizedBox(width: 12),

                    // Detail
                    Expanded(
                      child: Column(
                        crossAxisAlignment: CrossAxisAlignment.start,
                        mainAxisAlignment: MainAxisAlignment.spaceBetween,
                        children: [
                          // nama
                          Text(
                            'Store Name',
                            style: TextStyle(
                              fontWeight: FontWeight.w800,
                            ),
                          ),
                          SizedBox(height: 4),

                          // kategori
                          Text(
                            'Category',
                            style: TextStyle(
                              fontWeight: FontWeight.w600,
                              fontSize: 12,
                            ),
                          ),
                          SizedBox(height: 4),

                          // status buka
                          Row(
                            children: [
                              Icon(
                                Icons.watch_later_outlined,
                                size: 16,
                              ),
                              SizedBox(width: 4),
                              Text(
                                'Open Status',
                                style: TextStyle(
                                  fontWeight: FontWeight.bold,
                                  fontSize: 12,
                                  color: Colors.green,
                                ),
                              ),
                            ],
                          ),
                          SizedBox(height: 4),

                          // alamat
                          Row(
                            children: [
                              Icon(
                                Icons.location_on_outlined,
                                size: 16,
                              ),
                              SizedBox(width: 4),
                              Expanded(
                                child: Text(
                                  'Location',
                                  maxLines: 1,
                                  style: TextStyle(
                                    fontSize: 12,
                                  ),
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
                       RichText(
                          text: TextSpan(
                            children: [
                              TextSpan(
                                text: '5.0',
                                style: TextStyle(
                                  color: Colors.blue,
                                  fontSize: 15,
                                  fontWeight: FontWeight.bold,
                                ),
                              ),
                              TextSpan(
                                text: '/5',
                                style: TextStyle(
                                  color: Colors.blue,
                                  fontSize: 12,
                                ),
                              ),
                            ],
                          ),
                        ),
                    ],
                  ),
                ),
              ),
            ],
          ),
        )
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

 </details>
 
 

## # Carousel

 <details>
  <summary>View Widget</summary>
  
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
 
</details>



## # Text

  <details>
  <summary>View Widget</summary>
   
### 	• See More Text
![image](https://user-images.githubusercontent.com/90954993/163947902-34f756d9-397e-4b88-8f88-f848a84aabc0.png)
 
![image](https://user-images.githubusercontent.com/90954993/163947942-6032eb29-bb6b-4e0e-b6d8-8ec4b3e11b64.png)

<details>
 <summary> View Code </summary>
 
```

import 'package:flutter/gestures.dart';
import 'package:flutter/material.dart';

class ExpandableText extends StatefulWidget {
  const ExpandableText(
    this.text, {
    Key? key,
    this.trimLines = 2,
    this.style,
  })  : assert(text != null),
        super(key: key);

  final String text;
  final int trimLines;
  final TextStyle? style;

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
    final colorClickableText = Colors.blue;
    final widgetColor = Colors.black;
    TextSpan link = TextSpan(
        text: _readMore ? " Show more" : " Show Less",
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
        int? endIndex;
        final pos = textPainter.getPositionForOffset(Offset(
          textSize.width - linkSize.width,
          textSize.height,
        ));
        endIndex = textPainter.getOffsetBefore(pos.offset);
        var textSpan;
        if (textPainter.didExceedMaxLines) {
          textSpan = TextSpan(
            text: _readMore ? widget.text.substring(0, endIndex) : widget.text,
            style: widget.style ??
                TextStyle(
                  color: widgetColor,                  
                ),
            children: <TextSpan>[link],
          );
        } else {
          textSpan = TextSpan(
            text: widget.text,
            style: widget.style ?? null,
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
 
 </details>


 
 ## # Divider
 
 <details>
  <summary>View Widget</summary>
  

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

 </details>
 

 
## # Loading
 
 <details>
  <summary>View Widget</summary>


### 	• [Shimmer](https://pub.dev/packages/shimmer)
![image](https://user-images.githubusercontent.com/90954993/163972609-25cd4374-9059-42af-ae8c-095af92715e6.png)

<details>
 <summary> View Code </summary>
 
```
Shimmer.fromColors(
                baseColor: Colors.grey[500]!,
                highlightColor: Colors.grey[300]!,
                child: Container(
                  color: Colors.black.withOpacity(0.4),
                  height: 250,
                  width: 164,
                ),
              );
```
 
</details>
  
  ### 	• Skeleton

<details>
 <summary> View Code </summary>
 
```
import 'package:flutter/material.dart';

class Skeleton extends StatelessWidget {
  const Skeleton(
      {Key? key,
      this.height,
      this.width,
      this.radius,
      this.marginleft,
      this.marginTop,
      this.marginRight,
      this.marginBottom})
      : super(key: key);

  final double? height,
      width,
      radius,
      marginleft,
      marginTop,
      marginRight,
      marginBottom;

  @override
  Widget build(BuildContext context) {
    return Container(
      height: height,
      width: width,
      margin: EdgeInsets.fromLTRB(
          marginleft ?? 0, marginTop ?? 0, marginRight ?? 0, marginBottom ?? 0),
      decoration: BoxDecoration(
          color: Colors.black.withOpacity(0.4),
          borderRadius: BorderRadius.all(Radius.circular(radius ?? 0))),
    );
  }
}

class CircleSkeleton extends StatelessWidget {
  const CircleSkeleton(
      {Key? key,
      this.size = 24,
      this.marginleft,
      this.marginTop,
      this.marginRight,
      this.marginBottom})
      : super(key: key);

  final double? size, marginleft, marginTop, marginRight, marginBottom;

  @override
  Widget build(BuildContext context) {
    return Container(
      height: size,
      width: size,
      margin: EdgeInsets.fromLTRB(
          marginleft ?? 0, marginTop ?? 0, marginRight ?? 0, marginBottom ?? 0),
      decoration: BoxDecoration(
        color: Theme.of(context).primaryColor.withOpacity(0.4),
        shape: BoxShape.circle,
      ),
    );
  }
}


```
 
</details>
  
  ### 	• Shimmer Tile
![image](https://user-images.githubusercontent.com/90954993/168413763-33f53828-0501-4b75-925a-773ae6a3d5e1.png)

<details>
 <summary> View Code </summary>
 
```
import 'package:flutter/material.dart';
import 'package:shimmer/shimmer.dart';
import 'skeleton.dart';

class ShimmerTile extends StatelessWidget {
  const ShimmerTile({
    Key? key,
  }) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Shimmer.fromColors(
      baseColor: Colors.grey[500]!,
      highlightColor: Colors.grey[300]!,
      child: Container(
        margin: const EdgeInsets.fromLTRB(18, 12, 18, 12),
        child: Row(
          crossAxisAlignment: CrossAxisAlignment.center,
          children: [
            Skeleton(
              height: 84,
              width: 84,
              radius: 6,
            ),
            SizedBox(width: 16),
            Expanded(
              child: Column(
                crossAxisAlignment: CrossAxisAlignment.start,
                children: [
                  Skeleton(
                    height: 16,
                    radius: 2,
                  ),
                  SizedBox(height: 8),
                  Skeleton(
                    height: 16,
                    radius: 2,
                  ),
                  SizedBox(height: 8),
                  Skeleton(
                    height: 16,
                    width: 120,
                    radius: 2,
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}

```
 
</details>
  
   ### 	• Shimmer Card
![image](https://user-images.githubusercontent.com/90954993/168414071-fadfbbdf-a460-4587-b528-cd34bc7d6cb0.png)

<details>
 <summary> View Code </summary>
 
```
import 'package:flutter/material.dart';
import 'package:shimmer/shimmer.dart';
import 'skeleton.dart';

class ShimmerTile extends StatelessWidget {
  const ShimmerTile({
    Key? key,
  }) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Shimmer.fromColors(
      baseColor: Colors.grey[500]!,
      highlightColor: Colors.grey[300]!,
      child: Container(
        margin: const EdgeInsets.fromLTRB(18, 12, 18, 12),
        child: Row(
          crossAxisAlignment: CrossAxisAlignment.center,
          children: [
            Skeleton(
              height: 84,
              width: 84,
              radius: 6,
            ),
            SizedBox(width: 16),
            Expanded(
              child: Column(
                crossAxisAlignment: CrossAxisAlignment.start,
                children: [
                  Skeleton(
                    height: 16,
                    radius: 2,
                  ),
                  SizedBox(height: 8),
                  Skeleton(
                    height: 16,
                    radius: 2,
                  ),
                  SizedBox(height: 8),
                  Skeleton(
                    height: 16,
                    width: 120,
                    radius: 2,
                  ),
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}

```
 
</details>
 
### 	• Cached Image Network
Image loading waiting data from url
<details>
 <summary> View Code </summary>
 
```
CachedNetworkImage(
              imageUrl: 'https://images.unsplash.com/photo-1516259762381-22954d7d3ad2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8Y29kZXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60',
              imageBuilder: (context, imageProvider) {
                return Container(
                  height: 120,
                  decoration: BoxDecoration(
                    borderRadius: BorderRadius.circular(10),
                    image: DecorationImage(
                      image: NetworkImage(
                        'https://images.unsplash.com/photo-1516259762381-22954d7d3ad2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8Y29kZXxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60',
                      ),
                      fit: BoxFit.fill,
                      colorFilter: ColorFilter.mode(
                          Colors.black.withOpacity(0.3), BlendMode.darken),
                    ),
                  ),
                );
              },
              placeholder: (context, url) =>
                  Image.asset('assets/images/loader.gif'), // Loading icon
              errorWidget: (context, url, error) => Icon(Icons.error),
            ),
```
 
</details>
  
 
### 	• Loading Overlay

![image](https://user-images.githubusercontent.com/90954993/167959516-41fbc5ee-78e4-439a-9407-0ecd35698765.png)

<details>
 <summary> View Code </summary>
 
[Loading Overlay](https://github.com/ccprogrammer/my-widget/blob/main/Bulk%20Widget/loading_overlay.dart)
 
</details>
  
 </details>
 

 
## # Introduction / Onboarding Pages

 <details>
  <summary>View Widget</summary>
  
### 	• Common Intro Pages
![intro_1](https://user-images.githubusercontent.com/90954993/164210687-57f198d9-6fb5-4ff2-b789-a20888d1578c.png)
![intro_2](https://user-images.githubusercontent.com/90954993/164209426-88a94674-7f03-40ad-bfaf-9d624c653d10.png)
![image](https://user-images.githubusercontent.com/90954993/164211827-a750c496-5ed8-4962-9033-ff0f6b20aed7.png)


<details>
 <summary> View Code </summary>

[INTRODUCTION PAGES](https://github.com/ccprogrammer/my-widget/blob/main/Bulk%20Widget/introduction_page.dart)

</details>

 </details>


 
## # Splash Splash
 
 <details>
  <summary>View Widget</summary>
 
### • InkWell Splash ontap image
 ![image](https://user-images.githubusercontent.com/90954993/164356331-046a608c-0ffb-4c40-b96c-edbbc4655c67.png)

<details>
 <summary>View Code</summary>
 
 ```
 SizedBox(
              width: 60,
              height: 60,
            child: Material(
              color: Colors.transparent,
              child: InkWell(
                borderRadius: BorderRadius.circular(50),
                onTap: () {},
              ),
            ),
          ),
 
 example: 
 Container(
              margin: EdgeInsets.fromLTRB(0, 0, 0, 0),
              width: 227,
              height: 227,
              decoration: BoxDecoration(
                image: DecorationImage(
                  image: NetworkImage(
                      'https://images.unsplash.com/photo-1587207433549-7d796bccc6a2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8YnV0dG9ufGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60'),
                  fit: BoxFit.cover,
                ),
              ),
              child: Material(
                color: Colors.transparent,
                child: InkWell(
                  // borderRadius: BorderRadius.circular(50),
                  onTap: () {},
                ),
              ),
            ),
 
```
 
 </details>
  
 </details>
 
 
 
 ## # Gridview

 <details>
  <summary>View Widget</summary>
  
### 	• Common Grid
![image](https://user-images.githubusercontent.com/90954993/164387326-6a965d3a-bfd2-4cf8-ade8-fc08004731fc.png)

<details>
 <summary> View Code </summary>
 
```
GridView.builder(
        gridDelegate: SliverGridDelegateWithFixedCrossAxisCount(
          crossAxisCount: 3,
          crossAxisSpacing: 40,
          mainAxisSpacing: 40,
          // mainAxisExtent: 80,
        ),
        primary: false,
        shrinkWrap: true,
        itemCount: 9,
        itemBuilder: (context, index) {
          return Container(
            decoration: BoxDecoration(
              image: DecorationImage(
                image: NetworkImage(
                  'https://images.unsplash.com/photo-1592840496694-26d035b52b48?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8N3x8cGxheXN0YXRpb258ZW58MHx8MHx8&auto=format&fit=crop&w=500&q=60',
                ),
              ),
            ),
            child: Material(
               color: Colors.transparent,
               child: InkWell(
               onTap: () {
                 changeNoteIcon(noteIcon[index]['value']);
               },
              ),
            ),
          );
        },
      ),
```
 
</details>
 
 </details>
 
 
 
 ## # Rating & Review
 
 <details>
  <summary>View Widget</summary>

### 	• Rating & Review Box with [Rating Bar](https://pub.dev/packages/flutter_rating_bar) package
 ![image](https://user-images.githubusercontent.com/90954993/165880900-f3935fd1-943a-4cb0-ae61-012724cd0a9a.png)


<details>
 <summary> View Code </summary>
 
```

  Widget _buildRatingBox() {
    return Container(
      margin: EdgeInsets.fromLTRB(24, 20, 24, 0),
      padding: EdgeInsets.fromLTRB(20, 16, 20, 16),
      decoration: BoxDecoration(
        borderRadius: BorderRadius.circular(20),
        border: Border.all(
          color: Color(0xffD9D9D9),
          width: 1,
        ),
      ),
      child: Column(
        children: [
          Row(
            children: [
              Column(
                crossAxisAlignment: CrossAxisAlignment.start,
                children: [
                  RichText(
                    text: TextSpan(
                      children: [
                        TextSpan(
                          text: '5.0',
                          style: TextStyle(
                            color: Colors.black,
                            fontSize: 32,
                            fontWeight: FontWeight.bold,
                          ),
                        ),
                        TextSpan(
                          text: '/5',
                          style: TextStyle(
                            color: Colors.black,
                            fontSize: 15,
                          ),
                        ),
                      ],
                    ),
                  ),
                  SizedBox(height: 4),
                  RatingBar.builder(
                    initialRating: 5,
                    minRating: 0,
                    direction: Axis.horizontal,
                    glow: false,
                    allowHalfRating: false,
                    ignoreGestures: true,
                    itemCount: 5,
                    itemPadding: EdgeInsets.symmetric(horizontal: 0.0),
                    itemSize: 24,
                    onRatingUpdate: (value) {},
                    itemBuilder: (context, _) => Icon(
                      Icons.star,
                      color: Colors.amber,
                    ),
                  ),
                  SizedBox(height: 4),
                  Text(
                    'from 34 reviews',
                    style: TextStyle(
                      color: Color(0xff828382),
                      fontSize: 13,
                    ),
                  )
                ],
              ),
              SizedBox(width: 16),
              Expanded(
                child: Column(
                  mainAxisAlignment: MainAxisAlignment.start,
                  children: [
                    for (var i = 0.0; i < 5.0; i++)
                      Row(
                        children: [
                          RatingBar.builder(
                            initialRating: i,
                            minRating: 0,
                            direction: Axis.horizontal,
                            glow: false,
                            allowHalfRating: false,
                            ignoreGestures: true,
                            itemCount: 5,
                            itemPadding: EdgeInsets.symmetric(horizontal: 0.0),
                            itemSize: 16,
                            onRatingUpdate: (value) {},
                            itemBuilder: (context, _) => Icon(
                              Icons.star,
                              color: Colors.amber,
                            ),
                          ),
                          SizedBox(width: 8),
                          SizedBox(
                            width: MediaQuery.of(context).size.width * 0.19,
                            child: LinearProgressIndicator(
                              color: Colors.amber,
                              value: 1,
                              backgroundColor: Colors.grey,
                            ),
                          ),
                        ],
                      ),
                  ],
                ),
              ),
            ],
          ),
          Container(
            height: 42,
            margin: EdgeInsets.fromLTRB(0, 20, 0, 0),
            width: double.infinity,
            child: TextButton(
              onPressed: () {},
              style: TextButton.styleFrom(
                backgroundColor: Colors.transparent,
                // minimumSize:Size.zero,
                // padding: EdgeInsets.zero,
                side: BorderSide(
                  color: Constants.redonesmile,
                ),
                shape: RoundedRectangleBorder(
                  borderRadius: BorderRadius.circular(10),
                ),
              ),
              child: Text(
                'Write a review',
                style: TextStyle(
                  fontWeight: FontWeight.bold,
                  color: Constants.redonesmile,
                ),
              ),
            ),
          ),
        ],
      ),
    );
  }

```
 
</details>
 
 ### 	• [Rate Box](https://pub.dev/packages/flutter_rating_bar)
![image](https://user-images.githubusercontent.com/90954993/165892229-16ef82d2-d704-40ad-9809-b6835cee56f1.png)

<details>
 <summary> View Code </summary>
 
```
  double rating = 0.0;
  String ratingText = 'Choose Rating';
  Widget _buildRateBox() {
    return Container(
      margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
      padding: EdgeInsets.fromLTRB(0, 16, 0, 16),
      width: double.infinity,
      decoration: BoxDecoration(
        borderRadius: BorderRadius.circular(20),
        border: Border.all(
          width: 2,
          color: Color(0xffD9D9D9),
        ),
      ),
      child: Column(
        children: [
          RatingBar.builder(
            initialRating: 0,
            minRating: 0,
            direction: Axis.horizontal,
            glow: false,
            allowHalfRating: false,
            itemCount: 5,
            itemPadding: EdgeInsets.symmetric(horizontal: 4.0),
            updateOnDrag: true,
            itemBuilder: (context, _) => Image.asset(
              'assets/images/icon/new_design/star-2.png',
              width: 38,
              color: Colors.amber,
            ),

            // Icon(
            //   Icons.star,
            //   color: Colors.amber,
            // ),

            onRatingUpdate: (rating) => setState(() {
              this.rating = rating;
              // Pengkondisian text rating
              if (this.rating == 0.0) {
                ratingText = 'Choose Rating';
              } else if (this.rating == 1.0) {
                ratingText = 'Very Bad';
              } else if (this.rating == 2.0) {
                ratingText = 'Bad';
                ;
              } else if (this.rating == 3.0) {
                ratingText = 'Normal';
              } else if (this.rating == 4.0) {
                ratingText = 'Good';
              } else if (this.rating == 5.0) {
                ratingText = 'Excellent!';
              } else {}
            }),
          ),
          SizedBox(height: 12),
          Text(
            '${this.ratingText}',
            style: TextStyle(
              color: Colors.black,
              fontWeight: FontWeight.w800,
              fontSize: 16,
            ),
          ),
        ],
      ),
    );
  }

```
  
</details>
 
### 	• Write Review Box
![image](https://user-images.githubusercontent.com/90954993/165892292-5544b9c4-d21e-4384-ba19-21acf78d13c1.png)

<details>
 <summary> View Code </summary>
 
```

  Widget _buildReviewBox() {
    return Column(
      crossAxisAlignment: CrossAxisAlignment.start,
      children: [
        Container(
          margin: EdgeInsets.fromLTRB(24, 24, 24, 0),
          child: Text(
            'Write your review',
            style: TextStyle(
              color: Colors.black,
              fontWeight: FontWeight.w800,
              fontSize: 16,
            ),
          ),
        ),

        // Write review text area
        Container(
          margin: EdgeInsets.fromLTRB(24, 8, 24, 0),
          padding: EdgeInsets.fromLTRB(16, 4, 16, 4),
          width: double.infinity,
          constraints: BoxConstraints(
            minHeight: 100,
          ),
          decoration: BoxDecoration(
            color: Color(0xffF7F7F7),
            borderRadius: BorderRadius.circular(20),
          ),
          child: TextField(
            // controller: ratingReviewController,
            maxLines: null,
            onChanged: (value) {},
            decoration: InputDecoration(
              hintText: 'How is your overall experience?',
              hintStyle: TextStyle(
                color: Color(0xffB2B2B2),
              ),
              border: InputBorder.none,
            ),
          ),
        ),

        // Submit Review Button/sheet button
       Container(
        margin: EdgeInsets.fromLTRB(24, 16, 24, 24),
        width: double.infinity,
        height: 48,
        child: TextButton(
          onPressed: () {},
          style: TextButton.styleFrom(
            shape: RoundedRectangleBorder(
              borderRadius: BorderRadius.circular(8),
            ),
            backgroundColor: Colors.redAccent,
          ),
          child: Text(
            'Submit Review',
            style: TextStyle(
              color: Colors.white,
              fontWeight: FontWeight.bold,
            ),
          ),
        ),
      ),
      ],
    );
  }

```

 </details>
 
</details>
 
  ## # Font Family
  
  <details>
  <summary>View Widget</summary>

### 	• Adding font family to assets

<details>
 <summary> View Code </summary>
 
```
- download fonts from https://fonts.google.com/
 
- add to assets/fonts folder 
 
- in pubspec.yaml add this
   fonts:
    - family: Lato
      fonts:
        - asset: assets/fonts/Lato/Lato-Regular.ttf

    - family: Tapestry
      fonts:
        - asset: assets/fonts/Lato/Tapestry-Regular.ttf
 
- in Constants class/file add this (optional)
  static String lato = 'Lato';
  static String tapestry = 'Tapestry';
 
- in widget use this 
 TextStyle(
                  fontFamily: 'Lato' or Constants.lato,
                  color: Colors.white.withOpacity(0.87),
                  fontSize: 22.sp,
                ),
```
 
</details>
   
  </details>


 
 ## # Responsive
  
  <details>
  <summary>View Widget</summary>
 
 ### 	• [Screen Utils](https://pub.dev/packages/flutter_screenutil) Responsive Package

<details>
 <summary> View Code </summary>
 
```
  return ScreenUtilInit(
      designSize: Size(375, 812), // this size is from figma design frame size
      minTextAdapt: true,
      splitScreenMode: true,
      builder: (_) {
        return MaterialApp(
          debugShowCheckedModeBanner: false,
          home: SplashScreen(),
        );
      },
    );
 
add this after size number, example: height 100.h
height .h
width .w
margin/padding vertical .h 
margin/padding horizontal .w
font .sp
radius .r
```
</details>
 
  </details>
  
  ## # Image
  
<details>
 <summary> View Widget </summary>
 
### 	• Circle Image
 
![image](https://user-images.githubusercontent.com/90954993/167569995-de1145ec-6378-4ccf-a871-a47fdca91ddf.png)

<details>
 <summary> View Code </summary>
 
```
 Container(
            width: 62,
            height: 62,
            decoration: BoxDecoration(
              image: DecorationImage(
                image: NetworkImage(Const.dummyImage),
                fit: BoxFit.cover,
              ),
              color: Colors.white,
              shape: BoxShape.circle,
            ),
          ),
```
 
</details>
 
</details>
  


 
 ## # Git Template Title
  
<details>
 <summary> View Widget </summary>
 
### 	• Git Template Widget

<details>
 <summary> View Code </summary>
 
```

```
 
</details>
 
</details>

