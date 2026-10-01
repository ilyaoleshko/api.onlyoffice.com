import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

# CDocBuilderValue

Class used by ONLYOFFICE Document Builder for getting the results of called JS commands. It represents a wrapper for a JS object.

## Syntax

<Tabs groupId="lang">
    <TabItem value="python" label="Python">
        ```py
        class CDocBuilderValue:
            def __init__(self, value: bool)
            def __init__(self, value: int)
            def __init__(self, value: float)
            def __init__(self, value: str)
        ```
    </TabItem>
    <TabItem value="cpp" label="C++">
        ```cpp
        class CDocBuilderValue
        {
            CDocBuilderValue(const bool& value);
            CDocBuilderValue(const int& value);
            CDocBuilderValue(const unsigned int& value);
            CDocBuilderValue(const double& value);
            CDocBuilderValue(const char* value);
            CDocBuilderValue(const wchar_t* value);
        };
        ```
    </TabItem>
    <TabItem value="com" label="COM">
        ```cpp
        interface I_DOCBUILDER_VALUE : IDispatch
        {
            HRESULT CreateInstance([in] VARIANT_BOOL value);
            HRESULT CreateInstance([in] long value);
            HRESULT CreateInstance([in] double value);
            HRESULT CreateInstance([in] BSTR value);
        };
        ```
    </TabItem>
    <TabItem value="java" label="Java">
        ```java
        public class CDocBuilderValue {
            CDocBuilderValue(boolean value);
            CDocBuilderValue(int value);
            CDocBuilderValue(double value);
            CDocBuilderValue(String value);
            CDocBuilderValue(Object[] values);
        }
        ```
    </TabItem>
    <TabItem value="net" label=".Net">
        ```cs
        public class CDocBuilderValue
        {
            CDocBuilderValue(bool value);
            CDocBuilderValue(int value);
            CDocBuilderValue(unsigned int value);
            CDocBuilderValue(double value);
            CDocBuilderValue(String^ value);
        }
        ```
    </TabItem>
</Tabs>

## Methods

| Name                                  | Description                                                |
| ------------------------------------- | ---------------------------------------------------------- |
| [Call](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/Call.md)                       | Calls the specified Document Builder method.               |
| [Clear](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/Clear.md)                     | Clears the object.                                         |
| [CreateArray](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/CreateArray.md)         | Creates an array value. *(Python, Java only)*              |
| [CreateInstance](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/CreateInstance.md)   | Creates an instance of the CDocBuilderValue class. *(COM only)* |
| [CreateNull](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/CreateNull.md)           | Creates a null value. *(not used in COM)*                  |
| [CreateUndefined](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/CreateUndefined.md) | Creates an undefined value. *(not used in COM)*            |
| [Get](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/Get.md)                         | Returns an array value by its index.                       |
| [GetLength](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/GetLength.md)             | Returns the length if this object is an array/typed array. |
| [GetProperty](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/GetProperty.md)         | Returns a property of this object.                         |
| [IsArray](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/IsArray.md)                 | Returns true if this object is an array.                   |
| [IsBool](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/IsBool.md)                   | Returns true if this object is a boolean value.            |
| [IsDouble](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/IsDouble.md)               | Returns true if this object is a double value.             |
| [IsEmpty](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/IsEmpty.md)                 | Returns true if this object is empty.                      |
| [IsFunction](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/IsFunction.md)           | Returns true if this object is a function.                 |
| [IsInt](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/IsInt.md)                     | Returns true if this object is an integer.                 |
| [IsNull](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/IsNull.md)                   | Returns true if this object is null.                       |
| [IsObject](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/IsObject.md)               | Returns true if this object is an object.                  |
| [IsString](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/IsString.md)               | Returns true if this object is a string.                   |
| [IsTypedArray](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/IsTypedArray.md)       | Returns true if this object is a typed array. *(C++, COM, .Net only)* |
| [IsUndefined](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/IsUndefined.md)         | Returns true if this object is undefined.                  |
| [Set](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/Set.md)                         | Sets an array value by its index.                          |
| [SetProperty](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/SetProperty.md)         | Sets a property to this object.                            |
| [ToBool](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/ToBool.md)                   | Converts this object to a boolean value.                   |
| [ToDouble](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/ToDouble.md)               | Converts this object to a double value.                    |
| [ToInt](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/ToInt.md)                     | Converts this object to an integer.                        |
| [ToString](https://ilyaoleshko.github.io/api.onlyoffice.com/docs/document-builder/builder-framework/CDocBuilderValue/ToString.md)               | Converts this object to a string.                          |

:::note
**Java** uses camelCase method names: `call`, `clear`, `get`, `getLength`, etc.
:::
