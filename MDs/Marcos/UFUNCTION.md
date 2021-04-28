## UFUNCTION([...])

**DeprecatedFunction && DeprecationMessage**

```cpp
UFUNCTION(DeprecatedFunction, DeprecationMessage="")
void TempleFunc();
```









**CallInEditor**

被标记的C++函数签名，可以通过Details 面板中的按钮在编辑器中选中的实例上调用此函数。

被标记的函数签名必须是无参数的。

```cpp
UFUNCTION(CallInEditor, Category="Test")
void Test(void);

void ClassName::Test(void)
{}
```



**Category = "Tools|Constructors|etc"**

| 符号用于嵌套，划分类别，在Details面板中和蓝图中有不同的表现。



**BlueprintCallable** 

被标记的C++函数签名，可以在蓝图中被调用。



**BlueprintImplementableEvent**

该函数旨在被蓝图覆写，不要为其提供一个C++函数体，自动生成的代码中将会包含一个叫做 ProcessEvent 的thunk 来执行该函数

被标记的C++函数签名，不可以使用C++实现，必须在蓝图中实现。

```cpp
UFUNCTION(BlueprintCallable, BlueprintImplementableEvent, Category="Tool|Writer")
void Write();
```

在Event Graph 中查找 Event Write 即可获得覆写节点。



**BlueprintNativeEvent**

被标记的C++函数签名，可以使用C++和蓝图实现。

若蓝图实现与C++实现同时存在，优先使用蓝图实现；只有一个实现时则直接使用；都无实现时

```cpp
UFUNCTION(BlueprintCallable, BlueprintNativeEvent, Category="Tools")
void Read();

void ClassName::Read_Implementation()
{}
```



**BlueprintAuthorityOnly**



**BlueprintCosmetic**



**BlueprintPure**







**Client**



**CustomThunk**



**Exec**

被标记的C++函数签名可以从运行时控制台中执行。

只在特定类中使用才产生作用：

+ Pawns
+ PlayerControllers
+ PlayerInput
+ CheatManagers
+ GameModes
+ GameInstances
+ Overriden GameEngien Classes

```cpp
UFUNCTION(Exec)
SetValue(float Value);

void ClassName::SetValue()
{}


>
> SetValue 100
```



**NetMulticast**



**Reliable**



**SealedEvent**

被标记的函数签名，表示是密封的



**ServiceRequest**



**ServiceResponse**



**Server**



**Unreliable**



**WithValidation**