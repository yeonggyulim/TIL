# Primitive Components from React Native Library

### 1. View

### 2. Text

### 3. StyleSheet

### 4. FlatList
* required props
  1. data
  2. renderItem (function) => return 값이 render됨
  3. keyExtractor (function) => return 값이 key 값
* item들에 key를 줘야 tracking이 되어 한 item이 삭제되었을 때 모든 item들을 다 render하지 않음 (keyExtractor)

### 5. Button <==> (TouchableOpacity)
* Required props
    1. title
* Optional props
    1. onPress
* Show pre styled text

### 6. TouchableOpacity <===> (Button)
* No styling (We can style this)
* Fade out effect
* Show any kind of element inside of it
* Optional props
    1. onPress

### 7. Image
