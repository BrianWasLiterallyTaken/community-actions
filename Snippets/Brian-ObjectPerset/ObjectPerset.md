## Code
**Example Perset - `fruit_blender`**
```yaml
Apple: 5
Grapes: 6
Pineapple: 2

Blendable: true
```

**Fetching Values**
```js 
{set;apple;{find;{perget;fruit_blender};Apple: (\d+)}} // 5
{set;grapes;{find;{perget;fruit_blender};Grapes: (\d+)}} // 6
{set;pineApple;{find;{perget;fruit_blender};Pineapple: (\d+)}} // 2
{set;canBlend;{find;{perget;fruit_blender};Blendable: (\w+)}} // true
```

**Overwriting Values**
```js
{set;isBlendable;false} // Optional
{perset;PERSET_KEY;{replace;{perget;PERSET_KEY};Blendable: (\w+);Blendable: {get;isBlendable}}} // New value would be false
{perset;PERSET_KEY;{replace;{perget;PERSET_KEY};Blendable: (\w+);Blendable: false}} // Value will be false making our fetched 'canBlend' variable useless
```

**Adding Old and New values**
```js
{set;newApplesAdded;2} // Optional
{perset;PERSET_KEY;{replace;{perget;PERSET_KEY};Apple: (\d+);Apple: {math;{get;apple} + {get;newApplesAdded}}} // New value would be 7
{perset;PERSET_KEY;{replace;{perget;PERSET_KEY};Apple: (\d+);Apple: 7} // Value will be 7 making our fetched 'apple' variable also useless
```
