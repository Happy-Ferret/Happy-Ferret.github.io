---
layout: post
type: post
comments: true
title: "'OOP' in Lua"
summary: "The first in (most likely) a series of Lua related snippets.
         How to emulate basic class abstraction in a language that doesn't offer classes by default."  
# All dates must be YYYY-MM-DD format!
date: 2019-05-23 9:25:00 +0200
labels:
  - Lua 5.1
  - Scripting
  - Creative Coding
  - OOP
  - Design Patterns
---

```lua
-- Class definition
-- -> The attributes in curly braces are redunant, 
--    since we explicitly set them inside the constructor. 
--    I still include them. For brevity and convenience.
local Person = {name = nil, age = 0}
-- Re-route instance table lookups to the class table, to get methods.
-- -> Otherwise, we'd have to do "Person.__index.new(..)" 
--    rather than "Person.new(..)".
Person.__index = Person

-- Constructor method
function Person.new(name, age)
local self = setmetatable({}, Person)
self.__index = self
self.name = name or nil
self.age = age or 0
return self
end

-- Derived class method "greet()"
function Person.greet(self)
print("Hello, " .. self.name .. "!")
end

-- Object "henry" is an instance of class "Person".
henry = Person.new("Henry", 25)
-- Access class property "age".
print("Age: " .. henry.age)
-- Call class method "greet()".
henry:greet()

dorothy = Person.new("Dorothy", 68)
print("Age: " .. dorothy.age)
dorothy:greet()
```