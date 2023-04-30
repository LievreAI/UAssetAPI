# InterfacePropertyData

Namespace: UAssetAPI.PropertyTypes.Objects

Describes a reference variable to another object (import/export) which may be null ([FPackageIndex](./uassetapi.unrealtypes.fpackageindex.md)).

```csharp
public class InterfacePropertyData : ObjectPropertyData, System.ICloneable
```

Inheritance [Object](https://docs.microsoft.com/en-us/dotnet/api/system.object) → [PropertyData](./uassetapi.propertytypes.objects.propertydata.md) → [PropertyData&lt;FPackageIndex&gt;](./uassetapi.propertytypes.objects.propertydata-1.md) → [ObjectPropertyData](./uassetapi.propertytypes.objects.objectpropertydata.md) → [InterfacePropertyData](./uassetapi.propertytypes.objects.interfacepropertydata.md)<br>
Implements [ICloneable](https://docs.microsoft.com/en-us/dotnet/api/system.icloneable)

## Fields

### **Name**

The name of this property.

```csharp
public FName Name;
```

### **Ancestry**

The ancestry of this property. Contains information about all the classes/structs that this property is contained within. Not serialized.

```csharp
public AncestryInfo Ancestry;
```

### **DuplicationIndex**

The duplication index of this property. Used to distinguish properties with the same name in the same struct.

```csharp
public int DuplicationIndex;
```

### **PropertyGuid**

An optional property GUID. Nearly always null.

```csharp
public Nullable<Guid> PropertyGuid;
```

### **IsZero**

Whether or not this property is empty. If true, the body of this property will not be serialized in unversioned assets.

```csharp
public bool IsZero;
```

### **Offset**

The offset of this property on disk. This is for the user only, and has no bearing in the API itself.

```csharp
public long Offset;
```

### **Tag**

An optional tag which can be set on any property in memory. This is for the user only, and has no bearing in the API itself.

```csharp
public object Tag;
```

### **RawValue**

```csharp
public object RawValue;
```

## Properties

### **PropertyType**

```csharp
public FString PropertyType { get; }
```

#### Property Value

[FString](./uassetapi.unrealtypes.fstring.md)<br>

### **Value**

The main value of this property, if such a concept is applicable to the property in question. Properties may contain other values as well, in which case they will be present as other fields in the child class.

```csharp
public FPackageIndex Value { get; set; }
```

#### Property Value

[FPackageIndex](./uassetapi.unrealtypes.fpackageindex.md)<br>

### **ShouldBeRegistered**

Determines whether or not this particular property should be registered in the property registry and automatically used when parsing assets.

```csharp
public bool ShouldBeRegistered { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

### **HasCustomStructSerialization**

Determines whether or not this particular property has custom serialization within a StructProperty.

```csharp
public bool HasCustomStructSerialization { get; }
```

#### Property Value

[Boolean](https://docs.microsoft.com/en-us/dotnet/api/system.boolean)<br>

## Constructors

### **InterfacePropertyData(FName)**

```csharp
public InterfacePropertyData(FName name)
```

#### Parameters

`name` [FName](./uassetapi.unrealtypes.fname.md)<br>

### **InterfacePropertyData()**

```csharp
public InterfacePropertyData()
```