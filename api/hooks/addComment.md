# addComment

The `addComment` hook is triggered when a comment is added. It passes the ID of
the record and the data array as arguments and does not expect a return value.

> **Tag** Available from version 2.8.2.


## Parameters

1. *int* `$intId`

    ID of the new comment database record (Table `tl_comment`).

2. *array* `$arrSet`

    Data of the new comment record (not including the ID).


## Example

```php
<?php

// config.php
$GLOBALS['TL_HOOKS']['addComment'][] = array('MyClass', 'myAddComment');

// MyClass.php

/**
 * @param  integer  $intId       id of the comment
 * @param  array    $arrSet      The comments data
 * @param  Comments $objComments The Comments object
 * @return void                  No return value expected
 */
public function myAddComment($intId, $arrSet, Comments $objComments)
{
    // Do something
}
```


## More information


### References

- [system/modules/comments/classes/Comments.php](https://github.com/contao/core/blob/3.5.0/system/modules/comments/classes/Comments.php#L367-L374)


### See also

- [listComment](listComments.md) - triggered when comments are listed in the back end.
- [isAllowedToEditComment](isAllowedToEditComment.md) - triggered to determine permission on a comment in the back end.
