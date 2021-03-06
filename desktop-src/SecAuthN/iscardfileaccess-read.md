---
Description: The Read method reads and returns the specified data from a given file.
ms.assetid: 697b8dfa-754b-46cf-ab5c-1ac1d8ae47f2
title: ISCardFileAccess::Read method
ms.topic: reference
ms.date: 05/31/2018
topic_type: 
- APIRef
- kbSyntax
api_name: 
- ISCardFileAccess.Read
api_type: 
- COM
api_location: 
---

# ISCardFileAccess::Read method

\[The **Read** method is available for use in the operating systems specified in the Requirements section. It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The [Smart Card Modules](https://msdn.microsoft.com/library/Dd627652(v=VS.85).aspx) provide similar functionality.\]

The **Read** method reads and returns the specified data from a given file.

## Syntax


```C++
HRESULT Read(
  [in]  HSCARD_FILE  hFile,
  [in]  LONG         *lBytesToRead,
  [in]  SCARD_FLAGS  flags,
  [out] LPBYTEBUFFER *ppBuffer
);
```



## Parameters

<dl> <dt>

*hFile* \[in\]
</dt> <dd>

Handle of the open file to access.

</dd> <dt>

*lBytesToRead* \[in\]
</dt> <dd>

Length of data to be read (in) or number of bytes read (out). Returns list of files as an array of BSTRs.

</dd> <dt>

*flags* \[in\]
</dt> <dd>

Specifies whether secure messaging should be used.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC\_FL\_SECURE\_MESSAGING**
</dt> </dl> </dd> <dt>

*ppBuffer* \[out\]
</dt> <dd>

An [**IByteBuffer**](ibytebuffer.md) object containing the read data.

</dd> </dl>

## Return value

The method returns one of the following possible values.



| Return code                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S\_OK**</dt> </dl>          | Operation completed successfully.<br/> |
| <dl> <dt>**E\_INVALIDARG**</dt> </dl>  | Invalid parameter.<br/>                |
| <dl> <dt>**E\_POINTER**</dt> </dl>     | A bad pointer was passed in.<br/>      |
| <dl> <dt>**E\_OUTOFMEMORY**</dt> </dl> | Out of memory.<br/>                    |



 

## Remarks

For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).

In addition to the COM error codes listed above, this interface may return a [*smart card*](https://msdn.microsoft.com/library/ms721625(v=VS.85).aspx) error code if a smart card function was called to complete the request. For more information, see [Smart Card Return Values](authentication-return-values.md).

## Requirements



|                                     |                                                      |
|-------------------------------------|------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>          |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/> |
| End of client support<br/>    | Windows XP<br/>                                |
| End of server support<br/>    | Windows Server 2003<br/>                       |



## See also

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 




