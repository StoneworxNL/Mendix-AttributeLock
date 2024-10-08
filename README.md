# Mendix AttributeLock

**Mendix AttributeLock** is a Java action that helps enforce control over attribute and association changes by verifying if modifications are allowed before committing them.

## Dependencies
- None

## Key Features
- Validate if attribute or association changes are permitted before committing.

## Usage

1. **Add the Java Action**: Place the Java action in a *before commit* event of the entity. Ensure the return value of the action is returned within the event handler.
   
2. **Add an AllowedToChange Attribute**: Add an attribute named `AllowedToChange` to the entity you wish to monitor for changes.

3. **Specify Allowed Changes**: Before committing the object, populate the `AllowedToChange` attribute with the names of attributes and associations that are permitted to change, separated by a semicolon (`;`).

4. **Format for Attributes**: Attribute names should be entered exactly as they are defined.

5. **Format for Associations**: Association names must be prefixed with the module name followed by a dot (`.`).

6. **Wildcard for All Changes**: If all attributes and associations are allowed to change, you can use an asterisk (`*`) in the `AllowedToChange` attribute.

### Example:
If you want to allow changes to the attribute `FirstName` and the association `Customer_Order` in the Data module, set the `AllowedToChange` value to: `'FirstName;Data.Customer_Order'`

## Demo
Try the demo application:

- URL: [https://attributelock-sandbox.mxapps.io/](https://attributelock-sandbox.mxapps.io/)
- Username: `demo_user`
- Password: `WgZ2UL6vzZXv`

## Contributing

If you encounter issues, have suggestions, or want to request features, please visit our GitHub issues page:  
[Submit an Issue](https://github.com/StoneworxNL/Mendix-AttributeLock/issues)