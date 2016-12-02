# snippet-print

```java
@Test(expected = PrimaryAddressDeletionException.class)
public void testPrimaryAddressDeletion()
{
    int primaryAddress = customer.getPrimaryAddress().getId();
    addressService.deleteAddress(customer.getId(), primaryAddress.getId());
    // interaction checks
    Mockito.verify(dbService, times(1)).deleteDocument(customer.getPrimaryAddress().getId());
}
```
