# Reference
## mails
<details><summary><code>client.mails.<a href="src/usgm/mails/client.py">list</a>(...) -> MailPageDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List your mail items with filtering, search, sorting and cursor pagination
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.mails.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size, capped at 100.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque page cursor — the `next_cursor` of the previous response. Omit for the first page.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[typing.Union[MailsListRequestStatusItem, typing.Sequence[MailsListRequestStatusItem]]]` 
    
</dd>
</dl>

<dl>
<dd>

**mail_type:** `typing.Optional[typing.Union[MailsListRequestMailTypeItem, typing.Sequence[MailsListRequestMailTypeItem]]]` 
    
</dd>
</dl>

<dl>
<dd>

**folder_id:** `typing.Optional[int]` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**scan_status:** `typing.Optional[typing.Union[MailsListRequestScanStatusItem, typing.Sequence[MailsListRequestScanStatusItem]]]` — Filter by the item’s scan state; `none` selects items with no scan.
    
</dd>
</dl>

<dl>
<dd>

**sort:** `typing.Optional[MailsListRequestSort]` 
    
</dd>
</dl>

<dl>
<dd>

**arrived:** `typing.Optional[MailsListRequestArrived]` 
    
</dd>
</dl>

<dl>
<dd>

**is_read:** `typing.Optional[MailsListRequestIsRead]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.mails.<a href="src/usgm/mails/client.py">get</a>(...) -> MailDetailDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve full detail for one mail item, including dimensions, weight and folder
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.mails.get(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.mails.<a href="src/usgm/mails/client.py">update</a>(...) -> MailDetailDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Mark the item read/unread and/or move it into a folder
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.mails.update(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**is_read:** `typing.Optional[bool]` 
    
</dd>
</dl>

<dl>
<dd>

**folder_id:** `typing.Optional[str]` — Move the item to this folder. Pass null to remove it from its folder.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.mails.<a href="src/usgm/mails/client.py">archive</a>(...) -> MailDetailDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Move the item out of your active inbox into the archive
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.mails.archive(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.mails.<a href="src/usgm/mails/client.py">unarchive</a>(...) -> MailDetailDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Restore an archived item back to its previous inbox status
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.mails.unarchive(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.mails.<a href="src/usgm/mails/client.py">discard</a>(...) -> MailDetailDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Request the mailroom to discard the physical item; destructive, reverse with undiscard within 7 days after the discard request. After 7 days the mail item will be permanently and securely shredded and discarded
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.mails.discard(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.mails.<a href="src/usgm/mails/client.py">undiscard</a>(...) -> MailDetailDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancel a pending discard request and keep the item
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.mails.undiscard(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## scans
<details><summary><code>client.scans.<a href="src/usgm/scans/client.py">list</a>(...) -> ScanPageDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List your scan and open-and-scan requests, with filtering, search and pagination
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.scans.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size, capped at 100.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque page cursor — the `next_cursor` of the previous response. Omit for the first page.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[typing.Union[ScansListRequestStatusItem, typing.Sequence[ScansListRequestStatusItem]]]` 
    
</dd>
</dl>

<dl>
<dd>

**type:** `typing.Optional[typing.Union[ScansListRequestTypeItem, typing.Sequence[ScansListRequestTypeItem]]]` — `scan` (scan the item) or `open` (open it and scan the contents).
    
</dd>
</dl>

<dl>
<dd>

**mail_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**sort:** `typing.Optional[ScansListRequestSort]` 
    
</dd>
</dl>

<dl>
<dd>

**scanned:** `typing.Optional[ScansListRequestScanned]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.scans.<a href="src/usgm/scans/client.py">create</a>(...) -> ScanDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Request a scan or open-and-scan of a mail item; this is a billable action
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.scans.create(
    mail_id="mail_id",
    type="scan",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**mail_id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**type:** `CreateScanDtoType` — `scan` scans the item as-is; `open` opens it and scans the contents.
    
</dd>
</dl>

<dl>
<dd>

**instruction:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**is_expedited:** `typing.Optional[bool]` — Expedited handling — may incur an extra charge.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.scans.<a href="src/usgm/scans/client.py">get</a>(...) -> ScanDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve one scan request by its id, including status and AI label
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.scans.get(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.scans.<a href="src/usgm/scans/client.py">delete</a>(...) -> ScanDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a scan and remove its stored file; this cannot be undone
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.scans.delete(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.scans.<a href="src/usgm/scans/client.py">file</a>(...) -> ScanFileDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return a short-lived signed URL to download the scanned document; fetch it promptly
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.scans.file(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.scans.<a href="src/usgm/scans/client.py">summary</a>(...) -> ScanSummaryDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Return the AI-generated label and bullet summary of the scanned document
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.scans.summary(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.scans.<a href="src/usgm/scans/client.py">cancel</a>(...) -> ScanDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancel a scan request you no longer need. Valid only for scan requests in in_process status
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.scans.cancel(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## shipments
<details><summary><code>client.shipments.<a href="src/usgm/shipments/client.py">list</a>(...) -> ShipmentPageDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Read-only list of your shipment requests, filterable by type and status
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.shipments.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size, capped at 100.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque page cursor — the `next_cursor` of the previous response. Omit for the first page.
    
</dd>
</dl>

<dl>
<dd>

**type:** `typing.Optional[typing.Union[ShipmentsListRequestTypeItem, typing.Sequence[ShipmentsListRequestTypeItem]]]` 
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[typing.Union[ShipmentsListRequestStatusItem, typing.Sequence[ShipmentsListRequestStatusItem]]]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.shipments.<a href="src/usgm/shipments/client.py">get</a>(...) -> ShipmentDetailDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Read-only details of one shipment, including its packed mail items
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.shipments.get(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## folders
<details><summary><code>client.folders.<a href="src/usgm/folders/client.py">list</a>() -> FolderListDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

All your mail folders, returned unpaginated
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.folders.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.folders.<a href="src/usgm/folders/client.py">create</a>(...) -> FolderDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new mail folder with a name and optional color
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.folders.create(
    name="name",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**color:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.folders.<a href="src/usgm/folders/client.py">get</a>(...) -> FolderDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve one mail folder by its id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.folders.get(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.folders.<a href="src/usgm/folders/client.py">delete</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a folder and unfile its mail, which is not deleted
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.folders.delete(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.folders.<a href="src/usgm/folders/client.py">update</a>(...) -> FolderDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Rename a folder or change its color
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.folders.update(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**color:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## addresses
<details><summary><code>client.addresses.<a href="src/usgm/addresses/client.py">list</a>(...) -> AddressPageDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List your shipping and deposit addresses, optionally filtered by type
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.addresses.list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size, capped at 100.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque page cursor — the `next_cursor` of the previous response. Omit for the first page.
    
</dd>
</dl>

<dl>
<dd>

**type:** `typing.Optional[AddressesListRequestType]` — `shipping` = a shipment destination; `deposit` = where check deposits are sent.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.addresses.<a href="src/usgm/addresses/client.py">create</a>(...) -> AddressDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a new shipping or check-deposit address to your account
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.addresses.create(
    type="shipping",
    name="name",
    line1="line1",
    city="city",
    state="state",
    postal_code="postal_code",
    country="country",
    phone_number="phone_number",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**type:** `CreateAddressDtoType` — `shipping` = a shipment destination; `deposit` = where check deposits are sent.
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**line1:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**city:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**state:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**postal_code:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**country:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**phone_number:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**line2:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**line3:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**tax_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.addresses.<a href="src/usgm/addresses/client.py">getdefault</a>(...) -> AddressDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Get your default address for a given type, shipping or deposit
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.addresses.getdefault(
    type="shipping",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**type:** `AddressesGetDefaultRequestType` — `shipping` = a shipment destination; `deposit` = where check deposits are sent.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.addresses.<a href="src/usgm/addresses/client.py">get</a>(...) -> AddressDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve one shipping or deposit address by its id
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.addresses.get(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.addresses.<a href="src/usgm/addresses/client.py">delete</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete an address; this is destructive and cannot be undone
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.addresses.delete(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.addresses.<a href="src/usgm/addresses/client.py">update</a>(...) -> AddressDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update fields on an existing shipping or deposit address
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.addresses.update(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**type:** `typing.Optional[UpdateAddressDtoType]` — `shipping` = a shipment destination; `deposit` = where check deposits are sent.
    
</dd>
</dl>

<dl>
<dd>

**name:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**line1:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**line2:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**line3:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**city:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**state:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**postal_code:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**country:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**phone_number:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**tax_id:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.addresses.<a href="src/usgm/addresses/client.py">setdefault</a>(...) -> AddressDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Make this address the default for its type, replacing the previous default
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.addresses.setdefault(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## bank-accounts
<details><summary><code>client.bank_accounts.<a href="src/usgm/bank_accounts/client.py">bank_accounts_list</a>(...) -> BankAccountPageDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List your bank accounts used for check deposits
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.bank_accounts.bank_accounts_list()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Page size, capped at 100.
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `typing.Optional[str]` — Opaque page cursor — the `next_cursor` of the previous response. Omit for the first page.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.bank_accounts.<a href="src/usgm/bank_accounts/client.py">bank_accounts_create</a>(...) -> BankAccountDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a bank account for check deposits; account number is write-only
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.bank_accounts.bank_accounts_create(
    bank_name="bank_name",
    bank_state="bank_state",
    account_number="account_number",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**bank_name:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**bank_state:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**account_number:** `str` — Full account number. Write-only — reads return `account_number_last4`.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.bank_accounts.<a href="src/usgm/bank_accounts/client.py">bank_accounts_get</a>(...) -> BankAccountDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve one bank account by id, returning only the last 4 digits
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.bank_accounts.bank_accounts_get(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.bank_accounts.<a href="src/usgm/bank_accounts/client.py">bank_accounts_delete</a>(...)</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a bank account; this is destructive and cannot be undone
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.bank_accounts.bank_accounts_delete(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.bank_accounts.<a href="src/usgm/bank_accounts/client.py">bank_accounts_update</a>(...) -> BankAccountDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update the bank name, state, or account number on a bank account
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.bank_accounts.bank_accounts_update(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**bank_name:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**bank_state:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**account_number:** `typing.Optional[str]` — Full account number. Write-only — reads return `account_number_last4`.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## account
<details><summary><code>client.account.<a href="src/usgm/account/client.py">get</a>() -> AccountDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Your account profile, including name, email, status, and PMB number
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.account.get()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.account.<a href="src/usgm/account/client.py">mailingaddress</a>() -> MailingAddressDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Your current USGM address, including PMB number
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.account.mailingaddress()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## sandbox
<details><summary><code>client.sandbox.<a href="src/usgm/sandbox/client.py">seed</a>() -> SeedResultDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Populate your sandbox mailbox with sample mail items for testing
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.sandbox.seed()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="src/usgm/sandbox/client.py">seedmail</a>(...) -> SeedMailResultDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add one sample mail item to your sandbox mailbox, with optional overrides
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.sandbox.seedmail()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**sender_name:** `typing.Optional[str]` 
    
</dd>
</dl>

<dl>
<dd>

**mail_type:** `typing.Optional[SeedSandboxMailDtoMailType]` — Type of the seeded item. `LETTER` and `LARGELETTER` accept a `SCAN_REQUEST`; the rest accept an `UNBOXING_REQUEST`.
    
</dd>
</dl>

<dl>
<dd>

**weight:** `typing.Optional[float]` — Item weight, in pounds.
    
</dd>
</dl>

<dl>
<dd>

**measurement:** `typing.Optional[SeedSandboxMailDtoMeasurement]` — Item dimensions, in inches.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.sandbox.<a href="src/usgm/sandbox/client.py">completescan</a>(...) -> ScanDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Force a pending scan to completed in the sandbox for testing
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from usgm import Usgm
from usgm.environment import UsgmEnvironment

client = Usgm(
    token="<token>",
    environment=UsgmEnvironment.DEFAULT,
)

client.sandbox.completescan(
    id="id",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `str` 
    
</dd>
</dl>

<dl>
<dd>

**label:** `typing.Optional[str]` — Short document label the AI would produce, e.g. "Insurance". Set on the scan.
    
</dd>
</dl>

<dl>
<dd>

**summary:** `typing.Optional[typing.List[str]]` — Summary bullet points; retrievable via `GET /v1/scans/{id}/summary`.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

