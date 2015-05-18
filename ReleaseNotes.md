## Release Notes ##

### API Changes ###
  * v0.5
    * <font color='#FF0000'>not backwards compatible</font> - Deprecated getViewableFields, getUpdateableFields, and getCreatableFields accepting an sObject as input. (Fixes [Issue #6](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#6))
    * Added new functions getViewableFields, getUpdateableFields, and getCreatableFields accepting an sObjectType as input. (Fixes [Issue #6](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#6))
    * Added new functions isAuthorizedToView, isAuthorizedToCreate, isAuthorizedToUpdate, and isAuthorizedToDelete. (Fixes [Issue #5](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#5))
    * Added a describe info cache. (Fixes [Issue #3](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#3))
  * v0.4
    * insertAsUser and updateAsUser for a single SObject now return the object they actually used to insert/update the db. (Fixes [Issue #1](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#1))
    * <font color='#FF0000'>not backwards compatible</font> - insertAsUser, updateAsUser, and deleteAsUser for arrays of SObjects now return a new class object that can be used to get info such as Database.SaveResult[.md](.md), Database.DeleteResult[.md](.md), and the objects they actually used to insert/update the db. (Fixes [Issue #1](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#1))
    * Added insertAsUser and updateAsUser array operation functions that accept a list of fields as Schema.SObjectField[.md](.md) instead of String[.md](.md). This helps avoid limiters that were hit due to the user of the fields member variable in the String[.md](.md) variation. In addition it eliminates the namespace issues raised in [Issue #2](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#2). (Fixes [Issue #2](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#2) & [Issue #3](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#3))
  * v0.3
    * Added functions for DML array operations (insertAsUser, updateAsUser, deleteAsUser) to the SFDCAccessControl class. These functions allow to insert, update, and delete arrays of objects.
  * v0.2
    * Moved SFDCInvalidCharacterException class into the SFDCCharacter class. If you are currently using this class make sure to call it with the encapsulating class: `SFDCCharacter.SFDCInvalidCharacterException`.
    * Moved SFDCValidationException class into the SFDCValidator class. If you are currently using this class make sure to call it with the encapsulating class: `SFDCValidator.SFDCValidationException`.
  * v0.1
    * Initial release.

### All Changes ###
  * v0.5
    * <font color='#FF0000'>not backwards compatible</font> - Deprecated getViewableFields, getUpdateableFields, and getCreatableFields accepting an sObject as input. (Fixes [Issue #6](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#6))
    * Added new functions getViewableFields, getUpdateableFields, and getCreatableFields accepting an sObjectType as input. (Fixes [Issue #6](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#6))
    * Added new functions isAuthorizedToView, isAuthorizedToCreate, isAuthorizedToUpdate, and isAuthorizedToDelete. (Fixes [Issue #5](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#5))
    * Added a describe info cache. (Fixes [Issue #3](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#3))
  * v0.4 - June 9, 2010
    * insertAsUser and updateAsUser for a single SObject now return the object they actually used to insert/update the db. (Fixes [Issue #1](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#1))
    * <font color='#FF0000'>not backwards compatible</font> - insertAsUser, updateAsUser, and deleteAsUser for arrays of SObjects now return a new class object that can be used to get info such as Database.SaveResult[.md](.md), Database.DeleteResult[.md](.md), and the objects they actually used to insert/update the db. (Fixes [Issue #1](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#1))
    * Added insertAsUser and updateAsUser array operation functions that accept a list of fields as Schema.SObjectField[.md](.md) instead of String[.md](.md). This helps avoid limiters that were hit due to the user of the fields member variable in the String[.md](.md) variation. In addition it eliminates the namespace issues raised in [Issue #2](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#2). (Fixes [Issue #2](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#2) & [Issue #3](https://code.google.com/p/force-dot-com-esapi/issues/detail?id=#3))
  * v0.3 - April 19, 2010
    * Added functions for DML array operations (insertAsUser, updateAsUser, deleteAsUser) to the SFDCAccessControl class. These functions allow to insert, update, and delete arrays of objects.
    * Added HOWTO examples to each API function.
  * v0.2 - April 12, 2010
    * Updated javadocs.
    * Added test classes.
    * Moved SFDCInvalidCharacterException class into the SFDCCharacter class.
    * Moved SFDCValidationException class into the SFDCValidator class.
    * Changed the SFDCAccessControlException class to inherit directly from Exception.
  * v0.1 - March 25, 2010
    * Initial release.