
<template>
  <div class="flex h-screen w-full bg-gray-700">
  <div class="m-auto w-full px-5 md:w-1/3">
  <div class="pl-1 text-white font-medium text-2xl trackingwide
  text-center">
Inventory System
</div>
<form>
<inputElement
:labelName="'EMAIL'"
:labelId="'email'"
:inputType="'email'"
:model="email"
@input="email = $event"
:disabled="false"
/>
<inputElement
:labelName="'PASSWORD'"
:labelId="'password'"
:inputType="'password'"
:model="password"
@input="password = $event"
:disabled="false"
/>
<button type="button" class="
transition
duration-500
ease-in-out
bg-blue-600
rounded-xs
w-full
py-3
text-white
font-sans
font-bold
tracking-wide
hover:bg-blue-700
hover:text-gray-400
active:outline-none
focus:outline-none
"> SIGN IN </button></form>
</div>
</div>
</template>

<script>
  import Logo from '~/components/items/Logo.vue'
  import InputElement from "~/components/items/Input.vue";
  export default {

  transition:{
    name:"inventory",
    mode:"out-in",
    duration: { enter: 1000, leave: 500 },
    enterActiveClass: "animated fadeIn",
    leaveActiveClass: "animated fadeOut"
  },

    components: {
    Logo,
    InputElement
},
data: function(){
return{
email: "",
password: ""
}
}
}
</script>
