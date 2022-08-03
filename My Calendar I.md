# leetcode-solutions
all the leetcode solutions i have done till now
![image](https://user-images.githubusercontent.com/79332951/182679077-e774fc5d-1967-4726-b330-354418071d2f.png)
![image](https://user-images.githubusercontent.com/79332951/182679114-18897a0a-59a3-45c2-9e3f-b0633a1f7cd8.png)
```
class MyCalendar {
map<int,int> calendar;
public:
    MyCalendar() {
        
    }
    
    bool book(int start, int end) {
        auto next = calendar.upper_bound(start);
        if(next != calendar.end() && (*next).second < end)
          return false;
        calendar.insert({end,start});
        return true;
    }
};
```
