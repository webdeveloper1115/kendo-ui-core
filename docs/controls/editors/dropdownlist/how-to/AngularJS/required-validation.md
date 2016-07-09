---
title: Validate Lists by Using Required Attributes
page_title: Validate Lists by Using Required Attributes | Kendo UI DropDownList
description: "Learn how to use a required attribute to validate the Kendo UI DropDownList widget in AngualrJS applications."
slug: howto_validate_using_required_attributes_dropdownlist
---

# Validate Lists Using Required Attributes

The example below demonstrates how to use a required attribute, along with `ng-model`, to validate a DropDownList in AngularJS applications.

```html
<div ng-app="inputExample">
    <script>
     angular.module('inputExample', [ "kendo.directives" ])
       .controller('ExampleController', ['$scope', function($scope) {
         $scope.user = {country: ''};
       }]);
    </script>

  <div ng-controller="ExampleController">
    <form name="myForm">
      <label>
          Country:
          <select kendo-drop-down-list
                  k-option-label="'Select...'"
                  ng-model="user.country"
                  name="country"
                  required>
            <option>Albania</option>
            <option>Andorra</option>
            <option>Armenia</option>
            <option>Austria</option>
            <option>Azerbaijan</option>
            <option>Vatican City</option>
          </select>
      </label>
      <div role="alert">
        <span class="error" ng-show="myForm.country.$error.required">
         Required!</span>
      </div>
    </form>
    <hr>
    <tt>user = {{user}}</tt><br/>
    <tt>myForm.country.$valid = {{myForm.country.$valid}}</tt><br/>
    <tt>myForm.country.$error = {{myForm.country.$error}}</tt><br/>
  </div>
</div>
```

## See Also

Other articles on Kendo UI DropDownList:

* [DropDownList JavaScript API Reference](/api/javascript/ui/dropdownlist)
* [How to Cascade DropDownLists Using `ng-repeat`]({% slug howto_cascade_withngrepeat_distinct_values_dropdownlist %})
* [How to Automatically Adjust the Width of a DropDownList]({% slug howto_automatically_adjust_width_dropdownlist %})
* [How to Cascade from Multiple Parents]({% slug howto_cascade_multiple_parents_dropdownlist %})
* [How to Create DropDownLists with Long Items]({% slug howto_create_listswith_long_items_dropdownlist %})
* [How to Detect Input Change Events]({% slug howto_detect_input_change_events_dropdownlist %})
* [How to Detect Wrapper Blur Events]({% slug howto_detect_wrapper_blur_events_dropdownlist %})
* [How to Detect Wrapper Focus Events]({% slug howto_detect_wrapper_focus_events_dropdownlist %})
* [How to Move the Group Label on Top of Items]({% slug howto_move_group_label_ontopof_items_dropdownlist %})
* [How to Preselect Items]({% slug howto_preselect_items_dropdownlist %})
* [How to Update MVVM Bound Models on Load]({% slug howto_update_mvvm_model_onload_dropdownlist %})
* [How to Set DataSource Dynamically]({% slug howto_set_datasource_dynamically_dropdownlist %})
* [How to Remove Items]({% slug howto_remove_items_dropdownlist %})
* [How to Prevent Popup Closure on Scroll]({% slug howto_prevent_popup_closure_onscroll_dropdownlist %})
