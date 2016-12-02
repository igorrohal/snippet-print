# snippet-print

```java










		@Test(expected = PrimaryAddressDeletionException.class)
		public void testPrimaryAddressDeletion()
		{
			int primaryAddress = customer.getPrimaryAddress().getId();
			addressService.deleteAddress(customer.getId(), primaryAddress.getId());
			// interaction checks
			Mockito.verify(dbService, never()).deleteDocument(customer.getPrimaryAddress().getId());
		}
```
