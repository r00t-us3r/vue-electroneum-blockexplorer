<template>
  <div id="app">
    <Header />
    <TxPool />
    <Blocks />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import TxPool from './components/TxPool.vue'
import Blocks from './components/Blocks.vue'

export default {
  name: 'App',
  components: {
    Header,
    TxPool,
    Blocks
  }
}
</script>

<style>
@import 'https://fonts.googleapis.com/css?family=Quicksand:300,400,500,700';
@import 'https://fonts.googleapis.com/css2?family=Roboto';
body {
    margin: 0;
    padding: 0;
    color: #e9eef1;
    font-family: 'Roboto', sans-serif;
    background-color: #000;
    font-weight: 400;
    line-height: 1.5;
}

h1, h2, h3, h4, h5, h6 {
    text-align: center;
    font-size: 15px;
    line-height: 1.5;
    font-weight: 300;
    text-transform: none;
}

.center {
    margin: auto;
    width: 96%;
    max-width: 1400px;
}

table {
    width: 100%;
    border-spacing: 0;
    background-color: #000;
}

tr, li, #pages, .info {
    font-family: 'Roboto', sans-serif;
    font-size  : 15px;
    line-height: 2;
    font-weight: 100;
    height: 22px;
}

tr:hover {
    background-color: rgb(14, 14, 14);
}

tr:first-of-type {
    background-color: #111111;
    color: #e9eef1;
    font-weight: bolder;
}

td {
    border-top: 1px solid #050505;
}

table.net_info tr:hover td {
    background-color: #000000;
    border-top: 1px solid #000!important;
}

table.net_info tr td {
    background-color: #000000;
    border-top: 1px solid #000!important;
}

table.net_info tr:first-of-type {
    font-size  : 24px;
    font-weight: 400;
}

table.center {
    margin-left:auto;
    margin-right:auto;
}

#pages
{
    margin-top: 15px;
}

td {
    text-align: center;
}

a:link {
    text-decoration: none;
    color: #2ab1f3;
}

a:visited {
    text-decoration: none;
    color: #2ab1f3;
}

a:hover {
    text-decoration: underline;
    color: #2ab1f3;
}

a:active {
    text-decoration: none;
    color: #2ab1f3;
}

form {
    display: inline-block;
    vertical-align: middle;
    text-align: center;
}

.style-1 input[type="text"] {
    padding: 10px;
    font-size: 14px;
    border: solid 1px #0a0a0a;
    background-color: #242424;
    transition: box-shadow 0.3s, border 0.3s;
}
.style-1 input[type="text"]:focus,
.style-1 input[type="text"].focus {
    border: solid 1px #707070;
    box-shadow: 0 0 5px 1px #969696;
}
.style-1 input[type="submit"] {
    min-height: 36px;
    border: none;
    -webkit-appearance: none;
    padding: 10px;
    color: #fff;
    background-color: #2ab1f3;
    text-transform: uppercase;
    font-size: 14px;
}

.tabs {
    position: relative;
    min-height: 220px; /* This part sucks */
    clear: both;
    margin: 25px 0;
}

.tab {
    float: left;
}

.tab label {
    background: #111;
    padding: 10px;
    border: 1px solid #111;
    margin-left: -1px;
    position: relative;
    left: 1px;
}

.tab [type=radio] {
    display: none;
}

.content {
    position: absolute;
    top: 28px;
    left: 0;
    background: #111;
    right: 0;
    bottom: 0;
    padding: 20px;
    border: 1px solid #111;
    min-height: 215px;
}

[type=radio]:checked ~ label {
    background: #2ab1f3 ;
    border-bottom: 1px solid 2ab1f3;
    z-index: 2;
}

[type=radio]:checked ~ label ~ .content {
    z-index: 1;
}

input#toggle-1[type=checkbox] {
    position: absolute;
    /*top: -9999px;*/
    left: -9999px;

}
label#show-decoded-inputs {
    /*-webkit-appearance: push-button;*/
    /*-moz-appearance: button;*/
    display: inline-block;
    /*margin: 60px 0 10px 0;*/
    cursor: pointer;
    background-color: black;;
    color: white;
    width: 100%;
    text-align: center;
}

div#decoded-inputs{
    display: none;
}

/* Toggled State */
input#toggle-1[type=checkbox]:checked ~ div#decoded-inputs {
    display: block;
}

header {
    background-color: #000;
}
header img {
    margin: 10px 20px 10px 0;
    max-width: 250px;
    display: inline-block;
    vertical-align: middle;
}

html {
    font-family: 'Roboto', sans-serif;
    -webkit-font-smoothing: antialiased;
    text-rendering: optimizeLegibility;
}
</style>
