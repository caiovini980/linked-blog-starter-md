`Data validation` is the process to minimize the possibility of data errors (wrong values on attributes and properties, for example)

- `PreEditChange` 
	  - Chamado sempre que uma propriedade de um objeto na Unreal esta prestes a ser chamada
	  - Não funciona em structs
	  - Disponivel em qualquer UObject
	  - Função apenas de editor
	
- `PostEditChange`
	- Chamado depois da alteração
	- Disponivel em qualquer UObject
	- Função apenas de editor


- `UPROPERTY Specifiers`
	- `ClampMin` and `ClampMax` - Modifies the value directly
	- `UIMin` and `UIMax` - Don't change the value itself, only the UI on the editor. If the user change the value for something higher than the slider, it will work fine
	- `Delta` - Specify the variation of each movement on the slider
	- `EditCondition` - Only shows that property if some given condition is valid
	- `EditAnywhere` - This value can be modified on any versions of this class (on the default and on the instances)
	- `EditDefaultsOnly` - This value can be modified only on the default version of the class
	- `EditInstanceOnly` - This value can only be modified on the instances
	- `Multiline` - Displays a big chunk for the text area on the UI
	- `DisplayName` - Change the property displayed name on the editor
	- `AllowAbstract` - Here you can allow abstract classes to be pointed to an abstract class on the editor
	- `GetOptions` - Use just certain ([see minute 31:00](https://drive.google.com/file/d/1qJAozEucRb_bUazxyrhU29l8yj0Lxp0n/view?ts=6712543e)) options as a dropdown for a field value on the editor, 
	- 