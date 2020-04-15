<template>
    <div>
        <h1> Exercise 5 </h1>
         <!-- 1) Hook up the button to toggle the display of the two paragraphs. Use both v-if
         and v-show and inspect the elements to see the difference -->
         <div>
             <button @click="toggle = !toggle">Toggle (v-if)</button>
             <p v-if="toggle">You either see me ...</p>
             <p v-else>...or you see me</p>
             <button @click="show = !show">Toggle (v-show)</button>
             <p v-show="show">You either see me ...</p>
             <p>...or you see me</p>
         </div>
         <hr>
         <div>
             <!-- 2) Output an <ul> of array elements of your choice. Also print the index of each element. -->
            <ul>
                <li v-for=" (fruit, i) in fruits" :key="fruit"> {{ fruit }} ({{ i }})</li>
            </ul>
         </div>
         <hr>
         <div>
             <!-- 3) Print all key-value pairs pf the following object: {title: 'Lord of the Rings', author: 'J.R.R. Tolkiens',
             books: '3'}. Also print the index of each item. -->
            <ul>
                <li v-for="storybook in storybooks" :key="storybook.title">
                    {{ storybook }}
                </li>
            </ul>
         </div>
         <hr>
         <div>
             <!-- 4) Print the following object (only the values) and also create a nested loop for the array:
             {name: 'TESTOBJECT', data: [1.67, 1.33, 0.98, 2.21]} (hint: user v-for and v-if to achieve this) -->
             <ul>
                <li v-for="value in testData" :key="value.name">
                    <template v-if="Array.isArray(value)">
                        <div v-for="element in value" :key="element"> {{ element }}</div>
                    </template>
                    <template v-else>
                        {{ value }}
                    </template>
                </li>
            </ul>
         </div>
    </div>
</template>

<script>
export default {
    data: () => ({
        toggle: true,
        show: true, 
        fruits: ['apple', 'orange', 'banana', 'strawberry ', 'mango'],
        storybooks: {
                title: 'Lord of the Rings',
                author: 'J.R.R. Tolkiens',
                books: '3'
        },
        testData: {
                name: 'TESTOBJECT',
                data: [ 1.67, 1.33, 0.98, 2.21]
        }
        
    })
}
</script>