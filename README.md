# My Flutter Widget

<br />


### 	• Git Template

<details>
 <summary> View Code </summary>
 
```

```
 
</details>
 
 ## # AppBar
 
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
          width: width * 0.63,
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
          cancel == false
              ? IconButton(
                  onPressed: () {},
                  icon: Icon(
                    Icons.filter_list,
                  ),
                )
              : TextButton(
                  onPressed: () {
                    onCancel();
                  },
                  child: Text(
                    'Cancel',
                    style: TextStyle(
                      color: Colors.red,
                      fontSize: 16,
                      fontWeight: FontWeight.bold,
                    ),
                  )),
          SizedBox(width: 12),
        ],
      ),
      
```
 
 </details>
 
## # Icon

### • IconButton
Removed extra padding
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

## # List Tile

###	• Normal List Tile
![image](https://user-images.githubusercontent.com/90954993/163539806-b83e1040-8093-4f2a-8f85-fcf1d0f95c44.png)

<details>
 <summary>View Code</summary>
 
 ```
 Container(
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
```
 
</details>

###	• List Tile With Image
![image](https://user-images.githubusercontent.com/90954993/163541812-53d64dde-417d-44d9-8c9c-282319a205b0.png)

<details>
 <summary> View Code </summary>
 
```
Widget _buildSavedTile(i) {
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
                  data[i]['image'],
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
                      data[i]['nama'],
                      style: TextStyle(
                        fontWeight: FontWeight.w800,
                      ),
                    ),
                    SizedBox(height: 4),
                    Text(
                      data[i]['kategori'],
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
                          data[i]['is_open'] == true ? 'Open Now' : 'Close Now',
                          style: TextStyle(
                            fontWeight: FontWeight.bold,
                            fontSize: 12,
                            color: data[i]['is_open'] == true
                                ? Colors.green
                                : Colors.red,
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
                          data[i]['lokasi'],
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
          child: InkWell(
            onTap: () {
              data.removeAt(i);
              setState(() {});
            },
            borderRadius: BorderRadius.circular(50),
            child: Image.asset(
              'assets/images/icon/icon_saved.png',
              width: 24,
            ),
          ),
        ),
      ],
    );
  }
```
 
</details>

