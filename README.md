# Issues faced while using Roblox
## The current thread cannot access 'StreamingService' (lacking capability Assistant)
Seems to be a bug to be fixed by Roblox Dev team. Check here: https://devforum.roblox.com/t/the-current-thread-cannot-access-streamingservice-lacking-capability-assistant/3237401

```
if #child:GetChildren() > 0 then
  print("This Item has children")
end
```
You can fix this code by wrapping it in a pcall():
```
pcall(function()
  if #child:GetChildren() > 0 then
    print("This Item has children")
  end
end)
```
