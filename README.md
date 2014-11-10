ui-footable
===========
http://fooplugins.com/plugins/footable-jquery/

it realizes some functions of footable-jquery.

module name : uiFootable,uiFootablePagination

how to use:
```html
    <table ui-footable>
       <thead>
          <th data-toggle="true"></th>
          <th data-hide="phone"></th>
          <th data-hide="all"></th>
          <th data-hide="phone,tablet"></th>
        </thead>
       <tbody>
         <tr ng-repeat-start="item in items">
            <td>{{item.property}}</td>
            <td>{{item.property}}</td>
            <td>{{item.property}}</td>
            <td>{{item.property}}</td>
         </tr>
       </tbody>
       <tfoot>
         <tr ng-show="itemSize > 0">
           <td class="text-center" colspan="{{($columns|filter:{show:true}).length}}">
             <div class="ui-footable-pagination" ui-footable-pagination></div>
           </td>
          </tr>
         </tfoot>
    </table>
```
in parent controller,change values after load datas from server
```javascript
   $scope.pagination = { };
   $scope.pagination.itemSize = 12309;
   $scope.pagination.pageSize = uiFootablePageSize;
   $scope.pagination.pageNumber = Math.ceil($scope.pagination.itemSize / $scope.pagination.pageSize);
   $scope.pagination.currentPage = 1;
   $scope.pagination.lastPage = $scope.pagination.pageNumber;
```
