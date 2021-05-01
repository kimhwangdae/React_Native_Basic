# React_Native_Basic
React_Native 기본 개념 정리


## Stack Navigation
![스택 네비게이션](https://user-images.githubusercontent.com/59689327/116780948-abece480-aaba-11eb-9eb6-e8cfae3c4cc8.PNG)

``` 
 const Stack=createNavigator();
 <NavigationContainer> 
  <Stack.Navigator>
    <Stack.Screnn name="User" component={UserScreen}/>
  </Stack.Navigator>
 </NavigationContainer>
```
<Stack.Navigator> 사이에 띄워주고싶은 Screen들을 넣어줘야한다.<br>
Stack function은 Screen이라는 프로퍼티를 return할 때,<br>
Screen component를 명시해주는데, 이 때 명시된 component는 Stack 함수안에 있는 Screen 함수를 props 형태로 이용할 수 있다.<br>
위의 코드로 설명하자면 Stack 네비게이션 안에 있는 함수들을 UserScreen은 props 형태로 받게 된다는 말이다.<br>

![스텍 네비게이션2](https://user-images.githubusercontent.com/59689327/116780950-adb6a800-aaba-11eb-836a-25fa8a53512a.PNG)

```
<Button
  tilte="To Home Screen"
  onPress={()=>{
    this.props.navigation.navigate('Home')
  }}
/>
```

따라서, App.js에  <Stack.Navigator>사이에 <Stack.Screnn name="Home" component={HomeScreen}/> 을 추가해주면,<br>
위 코드에서 같이 props로 넘어온 navigation.navigate 함수로 인해 name이 'Home'인 Srceen으로 이동하게 되는것이다.
