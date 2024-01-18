import { useEffect, useState } from 'react';
import React from 'react';
import { View, Text, FlatList } from 'react-native';

const YourComponent = () => {
  const [count, setCount] = useState("");
  useEffect(()=>{
    alert('go to effect screen');
},[3])
  const data = [
    { id: '1', text: 'farwa' },
    { id: '2', text: 'isha' },
    { id: '3', text: 'mehak' },
    
  ];
  const renderItem = ({ item }) => (
    <View>
      <Text>{item.text}</Text>
    </View>
  );

  return (
    <View>
      <FlatList
        data={data}
        renderItem={renderItem}
        keyExtractor={item => item.id}
      />
    </View>
  )}
  export default  YourComponent;
