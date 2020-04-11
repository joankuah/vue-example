<template>
    <div>
        <h1>Exercise 4</h1>
        <!-- 1) Start the Effect with the Button. The Effect should alternate the "highlight" or "shrink" class on each new
        setInterval tick (attach respective class to the div with id "effect" below) -->
        <div>
            <button @click="startEffect">Start Effect</button>
            <div :class="['effect', toggleCss]" ></div>
        </div>
        <hr>
        <div>
            <!-- 2) Create a couple of CSS classes and attach them via the array syntax -->
            <div :class="[class1, class2, class3 , toggleClass]">{{ whatClassAmI() }}</div>
            <div>
                <button @click="class1 = !class1, class2 = false, class3 = false">class 1</button>
                &nbsp;
                <button @click="class2 = !class2, class1 = false, class3 = false">class 2</button>
                &nbsp;
                <button @click="class3 = !class3, class1 = false, class2 = false">class3</button>
            </div>
        </div>
        <hr>
        <div>
            <!-- 3) Let the user enter a class (create some example classes) and attach it -->
            <div>
                <input type="text" v-model="input">
                <div :class="input"></div>
            </div>
        </div>
        <hr>
        <div>
            <!-- 5) Repeat 3) but now with values for styles (instead of class names). Attach
            the respective styles -->
            <div>
                <input type="text" v-model="color">
                <div :class="color"></div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data: () => ({
        toggle : false,
        hasEffectStarted: false,
        class1: false,
        class2: false,
        class3: false,
        input: '',
        color: ''
    }),
    methods: {
        startEffect: function() {
            //setInterval
            const self = this
            self.hasEffectStarted = true
            this.intervalid1 = setInterval( function() {
                self.toggle = !self.toggle
            }, 2000)
            
        },
        whatClassAmI: function() {
            
            if(this.class1) {
                return "I am class 1"
            } else if (this. class2) {
                return "I am class 2"
            } else if (this.class3) {
                return "I am class 3"
            } else {
                return " I have no class :("
            }

        }
    },
    computed: {
        toggleCss: function() {
            return {
                effect: !this.hasEffectStarted,
                highlight: this.toggle && this.hasEffectStarted,
                shrink: !this.toggle && this.hasEffectStarted
            }
        },
        toggleClass: function() {
            return {
                class1: this.class1,
                class2: this.class2,
                class3: this.class3
            }
        },
        myStyle: function() {
            return {
                backgroundColor: this.color
            }
        }

    }
}
</script>

<style>
.effect {
    width: 100px;
    height: 100px;
    border: 1px solid black;
}

.highlight {
    background-color: red;
    width: 200px;
}

.shrink {
    background-color: gray;
    width: 50px;
}

.class1 {
    background-color: pink;
    width: 100px;
    height: 100px;
    margin: auto;
    border: 1px solid black;
}

.class2 {
    background-color: lightblue;
    width: 100px;
    height: 100px;
    margin: auto;
    border: 1px solid black;
}

.class3 {
    background-color: lightgreen;
    width: 100px;
    height: 100px;
    margin: auto;
    border: 1px solid black;
}
</style>