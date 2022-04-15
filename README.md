# My Flutter Widget

<br />

### # IconButton
Removed extra padding
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

### # List Tile
![image](https://user-images.githubusercontent.com/90954993/163539806-b83e1040-8093-4f2a-8f85-fcf1d0f95c44.png)


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
