#Using ESX Functions with FiveM JS

[Forum Thread]()

Recently I've been writing all of my scripts in JS, with FiveM the main economy framework is ESX. Writing ESX functions inside of JS is very easy and today Im going to show you how to do it!
Calling Shared Object.


###Calling Shared Object.
###Getting a players cash.
###Creating a Menu.

JS:
let ESX = null;
emit("esx:getSharedObject", (obj) => ESX = obj);
LUA:
ESX = nil
TriggerEvent('esx:getSharedObject', function(obj) ESX = obj end)
Client-
JS:
let ESX = null;
emit("esx:getSharedObject", (obj) => ESX = obj);
LUA:
ESX = nil

Citizen.CreateThread(function()
while ESX == nil do
TriggerEvent('esx:getSharedObject', function(obj) ESX = obj end)
Citizen.Wait(0)
end
end)
Here you can use client functions like ESX.ShowNotification, which is the same for LUA and JS.
Getting a xPlayer's cash (server)
JS:
let xPlayer = ESX.GetPlayerFromId(source);
let cash = xPlayer.getMoney();
console.log(cash);
LUA:
local xPlayer = ESX.GetPlayerFromId(source)
local cash = xPlayer.getMoney()
print(cash)
Creating a Menu (client)
JS:
ESX.UI.Menu.Open('default', GetCurrentResourceName(), 'menuname',{
title: 'Here, the menu title',
align: 'top-left',
elements: [
{label: 'Here, field 1 of the menu', value: 'test'},
{label: 'Fields 2', value:'fields2'},
{label: 'Fields 3', value: 'fields3'}
]
}, function(data, menu) {
console.log(data.current.value);
}, function(data, menu) {
menu.close();
});
