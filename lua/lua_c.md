# lua && c

> gcc test.c -I./lualib/include -L./lualib/lib -llua54

```c
lua_State *L = luaL_newstate(); // create Lua vm
luaL_openlibs(L); // open Lua vm and load all standard lib in lua
luaL_dofile("fileName"); // load file xxx, and run
lua_getglobal(L, "functionName"); // call function
lua_pushnumber(L, number);
lua_call(L, x, y); // declare user x parametes, y return values
lua_pop(L, x);
lua_close(L);
```
 