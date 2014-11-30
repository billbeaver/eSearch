# Enhanced Search Widget

[View live app here](http://gis.calhouncounty.org/FlexViewer3.1/index.html?config=config-eSearch.xml&esearch=2&slayer=3&exprnum=1)

[![Image of Enhanced Search Widget](https://raw.github.com/rscheitlin/eSearch/master/Preview.jpg "Example Enhanced Search Widget app")](http://gis.calhouncounty.org/FlexViewer3.1/index.html?config=config-eSearch.xml&esearch=2&slayer=3&exprnum=1)

## Version Updates
Version 3.7 - 10/29/2014
* Recompiled for Flex Viewer 3.7
* Assets folder is now searched for based on the location of the compiled widget and not the configuration file.
* This widget now has a GUI in App Builder!

Version 3.6.10 - 10/20/2014
* Fixed issues with searching MultiPoint Geometry.
* Fixed error 1009 when preforming a graphical search when the widget is initially opened.

Version 3.6.9 - 9/12/2014
* Made some big code changes that now allows the esri print service able to print the search results with the proper symbology.
* Fixed and issue when the first layer in the xml has uniquevalsfromfield and you use a url search a bug occurred.

Version 3.6.8 - 6/23/2014
* Fixed a bug with sum field when the format was currency.
* If the selectedgraphicaltool has been specified or you have already used a graphical search tool
  when you switch to the graphical search tab that tool will be selected automatically.
* Uniquevalsfromfield now optimized to use returnDistinctValues if the server version is 10.1 or greater 
  (this means no paging and faster unique values). Thanks to Daryl Anderson for this idea.
  
Version 3.6.7 - 5/29/2014
* Fixed a few graphical query issues introduced in 3.6.6. 
* Fixed hyperlinkaliastext not being used with working with related data.
* Added another localized text option to xml.

Version 3.6.6 - 5/22/2014
* Fixed URL Query Bug when a search is made and no results are found. 
* Fixed csv and txt file extension bug in Fixed datagrid export.

Version 3.6.5 - 4/3/2014
* Changed export GUI design to minimize footprint.
* Added buffer support to eDraw, eLocate and pointBuffer.

Version 3.6.4 - 3/3/2014
* Fixed issue with field formatting not staying specific to the field it was set for.
* csv and txt exports now export proper linefeed based on OS.
* Added exportnumbersasformattedstrings attribute to enableexport tag. See pdf for explanation.
* Added popuplinktype attribute to link tag. See pdf for explanation.

Version 3.6.3 - 2/26/2014
* Fix major bug with uniquevalsfromfield not returning all records in some cases.

Version 3.6.2 - 2/20/2014
* Fix issue with disableinpopup in datagrids.
* Fix issue with UNC links that have icons specified not working in my popups.
* Fix issue with union geoms function and some multi ring polygons. 
  Special thanks to Leonardo Ara�jo for the code contribution.
* Added more configurable messages for widget internationalization.
* You can now configure the buffer graphic to remain visible after the search.

Version 3.6.1 - 12/19/2013
* Fixed issue With search layer symbology not showing when using a URL search until a selection was made in the datagrid.
* Unique values from field now honors the layers definition expression.

Version 3.6 - 12/19/2013
* Recompile for ArcGIS Viewer for Flex Version 3.6

Version 3.5.4 - 11/5/2013
* Fixed issue With dropdownlists sizes that was introduce in 3.5.3.

Version 3.5.3 - 10/22/2013
* Fixed issue With preload="minimized" and the dropdownlists.
* Fixed issue with SubTypes and Domains assigned to subtypes.
* Fixed issue with text qualify userlists and the all option.

Version 3.5.2 - 10/11/2013
* Fixed issue hyper link grid fields and version 3.5.1.
* Added ability to text qualify userlists that contain comma in their values.

Version 3.5.1 - 10/11/2013
* Fixed issue with tables and version 3.5.

Version 3.5 - 10/7/2013
* Added sub selection color for subselecting results from he datagrid.
* Fixed Relate error when using fields all="true"
* Fixed issue with choose relate dialog not closing using the X in the upper right corner.
* When buffering during a graphical search, the buffer graphic is now removed after the search is complete.

Version 3.4 - 7/25/2013
* memory leak fix
* Link alias added to photo caption
* Issue with type and coded domains fixed
* Issue with field used as hyperlinkaliastext and not being defined in the field list fixed
* Datagrid autosizing will use the hyperlinkaliastext fields value if larger than the alias text

Version 3.3.3 - 6/4/2013
* Fixed issue where if relate only has one field and it is a hyperlink field the field is added twice and neither is a hyperlink field.
* Fixed issue with zoom and relates
* Better validation of whether the search layer exists in the map and a token is already specified.
* Make 4 additional attempts to get unique values from a field before failing

Version 3.3.2 - 5/15/2013
* Added textqualifier tag for defining the character that will be used in the export datagrid to signify that the
field contents are a string to programs like Excel�.
* Added removeserchlayersminmaxscale tag that specifies whether or not to remove the
MinScale and MaxScale of the layer that is set on the particular layer from ArcGIS Server.

Version 3.3.1 - 5/10/2013
* Better error trapping for missing zoomscale on relates
* Add empty strings choice in dropdown for expression from a domain field that is set to isValueRequired false
* Added disable links in popups attribute

Version 3.3- 5/6/2013
* Recompiled for Flex Viewer 3.3

Version 3.2.3 - 4/30/2013
* Added enablemultigraphicssearch
* Added enableincludetextsearch
* Added enableaddtollerance
* Added enablegraphicsbuffering
* Fixed disablelinkifnull issue
* Relate tab name is set to relate label from xml
* Fixed issue using uniquevalsfromfield when only having tables configured

Version 3.2.2 - 4/3/2013
* Fixed bug where selection layer would sometimes show in the layer list/Map switcher widgets with some generic name.
* Fixed issue with table to related features relate datagrid row click or other errors.
* Added support for relates to have a zoomscale or zoompercent just like layers.

Version 3.2.1 - 4/1/2013
* Added back the wait cursor that is displayed when a search is executing.
* Added zoom to supports for row clicks in a related table (if the related data has geometry, both feature to table and table to feature supported).

Version 3.2 - 3/22/2013
* Recompiled for Flex Viewer 3.2
* If hyperlinkaliastext is a field that has a linkprefix and or suffix then do not include the linkprefix and or suffix in the alias text.

Version 3.1.12 - 3/6/2013
* Fix bug where useproxy was not being honored in the UniqueValsfromField.
* Fix spelling of disablelinksifnull attribute.
* Allow hyperlinkaliastext to use a field as well as a hard coded string.
* Allow link alias to use a field as well as a hard coded string.

Version 3.1.11 - 3/2/20123
* Fixed RTE (runtime error) with related data when relate has subtype.
* Graphical search buttons now toggle.
* Applied workaround for Google Chrome datagrid print blank page issue.

Version 3.1.10 - 2/26/2013
* Changed appearance of multiple expressions to have an alternating background color so they are easy to distinguish for one another.
* Fixed potential bug with buffering by adding spatial reference to buffer request.
* Fixed RTE (runtime error) with Apply Buffer before a search is performed.
* Documented useproxy for layers.

Version 3.1.9 - 2/19/2013
* autoopendatagrid is now honored by the fixed datagrid as well as the floating datagrid.
* Drop down lists no longer initalize with no item selected as they did in versions 3.1.7 & 8.
* Handle IN SQL statements in expressions and automatic single quoting of values if expression is expecting strings.
* Fixed escaping of single quotes in user values if more than one exist (i.e. O'Malley and O'Leary Inc).
* Added integration with the Enhanced Locate Widget.
* Fixed issue where widget title button for results was not always selected (shown with underline) when results view was activated.

Version 3.1.8 - 2/5/2013
* Fixed Localization issue with export2csvoptionlabel and export2txtoptionlabel
* Added autosubmit to expression values to allow control over whether a dropdown list automatically fires the search upon selection and textbox when the enter key is pressed. The default is true if this attribute is not used.

Version 3.1.7 - 1/30/2013
* Fixed issue with required fields and dropdownlist executing search before all required fields are completed.
* Re-use a map layer token from the identify manager if the same layer is configured for a search.
* Honor gridfield and gridhyperlinkfield order set in the eSearchWidget.xml (add in order specified).

Version 3.1.6 - 1/25/2013
* Fixed major bug introduced in 3.1.5 with adding and removing form selections
* Fixed bug, when clicking on a popup the datagrid opens.
* Fixed bug when using a hyperlink field in the datagrid with a hyperlinkgridicon specified and error occurs.

Version 3.1.5 - 1/22/2013
* Fixed bug when user does not have ANY layer setup for spatial search.
* Fixed more layer symbology issues.
* Added configuration options for selecting buffer units and distance from xml.

Version 3.1.4 - 1/15/2013
* Fixed a bug when you clear the results and then choose add to results and make a selection.

Version 3.1.3 - 1/11/2013
* Fixed some issues with relates and uniquevalsfromfield when using tokens.
* Fixed some issues if the layers url contains the token.

Version 3.1.2 - 1/2/2013
* When features are added to the selection they appear at the top of the Widgets results list.
* When features are removed the order of the results remains the same minus the removed results.

Version 3.1.1 - 12/19/2012
* Updated some code for API Version 3.1
* Added Token Element to layers and tables
* Fixed some bugs with layer zoom settings.
* Removed geometryservice from eSearchWidget.xml as it gets this from the main config.xml now.
* Added some error trapping to URL Searches using improper parameters
* Changed the URL Search parameter to esearch (was search) as esri is now using search for their
  purposes and it was conflicting with mine.

Version 3.0.16 - 12/3/2012
* Fixed an issue with blanks (when using isrequired="true") and empty strings be treated
  as equal when using uniquevalsfromfield.
* uniquevalsfromfield can now use a datefield and used the dateformat and useutc attributes.

Version 3.0.15 - 11/28/2012
* Fixed an issue when printing after a search and the search layer did not have individual
  layer symbology specified in the eSearchWidget.xml
* Fixed issue where you could not use just tables in the eSearchWidget.xml
* Fixed issue where clicking the clear button before running a search produces an error.
* Fixed issue where new/add/remove selection button is not in the GUI when there is only
  one layer configured.
* Removed the Zoom All button when the results are a table.
* Validate the returned geometry before attempting to zoom to all selected features.

Version 3.0.14f - 11/15/2012
** Hot fix for uniquevalsfromfield now are aware of isrequired attribute and add a blank entry
   in the drop down if necessary.
** Hot fix for Added support for disabling popups completely for this widget.
** Hot fix for bug where if more than one uniquevalsfromfield is used in the first expression
   only one will populate the dropdown.

Version 3.0.14 - 11/14/2012
* Fixed bug where if more than one uniquevalsfromfield was used in an expression
  Only one would populate the dropdown.
* uniquevalsfromfield now are aware of isrequired attribute and add a blank entry
  in the drop down if necessary.
* Added delay for mouseover in datagrids to allow user to exit datagrid and choose
  a button from the popup
* The popup shown from the search results and datagrid is the same popup that gets
  displayed when you click on the search graphic on the map.
* Added the ability to add and remove from current selection as well as create a new
  selection (which is the default).
* Fix bug where individual layers symbology specified in the eSearchWidget.xml was
  not being used with certain spatial searches.
* Added support for disabling search widget results (just use <disablebuttons>result</disablebuttons>).
* Added support for disabling popups completely for this widget.

Version 3.0.13 - 10/25/2012
* You can now print from the datagrid (floating or fixed). The Print output is properly paginated
  based on the number of columns (and their widths) and the number of rows. The print output has
  several configurable option for header colors, footer elements, etc. The print honors any sort
  applied to the datagrid.
* Export to csv and text now honors the sort applied to the datagrid.
* Fixed bug with resetting required fields when the search is cleared.

Version 3.0.11 - 10/17/2012
* Added uniquevalsfromfield as a source for search drop down (like usedomain and userlist options).
* Changed the default spatialreference in the xml to 102100.
* Fixed bug with spatial search using symbology from first text search layer instead of chosen spatial
  search layer.
* Changed the line width stepper in the GUI to use whole numbers (thanks to Bjorn for point this out).

Version 3.0.10 - 9/24/2012
* Added annimation to buffer graphic properties button.
* Added usesubtype as a source for search drop down (like usedomain option).
* Updated Enhanced Search Widget XML Configuration.pdf to include info on visible property
  of fields element.
* Fixed bug with float datagrid not honoring enable export option in all situations.

Version 3.0.9 - 9/13/2012
* Added an auto sync between the text search layer and the graphical serach layer dropdowns.
* Depreciated the disablerelatestabinfixed attribute infavor of automatically setting the
  visibility of the relates tab for the fixed datagrid based on, if the layer has relates 
  configured or not.
* Fixed datagrid now has configuration options for height and animation duration. Thanks to Kenny Horan
* Added an auto hide checkbox on the fixed datagrid to toggle the auto hide capability.
* Disablelinksifnull attribute now checks for empty strings as well as null values in the link fields.

Version 3.0.8 - 9/4/2012
* Added attribute to not display links that have null values.
* Fixed bug with sorting on joined data.
* Fixed bug with datefomat not being specified throwing error.
* Added a isvaluerequired attribute to expression values and expressions (see documentation for details).
* Added ability to define symbology at the layer level and widget level. 

Version 3.0.7 - 8/21/2012
* Tab labels are now configurable in the Fixed data grid (use the SearchWidgetFixedDG.xml).
* Fixed nobufferoutlincolor label being ignored in the eSearchWidget.xml
* Fixed show and hide animation on Fixed Datagrid.
* Fixed datagrid (if autohide) will show when a search is executed and hide with results are cleared.
* If multi field expressions are used, now all fields DO NOT have to be filled.
* Fixed PopUp Attachment Issue.

Version 3.0.6 - 8/15/2012
* Fixed issue with field date formatting.
* Fixed issue with fixed datagrid that is hidden, showing when a popup is shown the first time.
* Fixed issue where buffering would not work (spatial or graphical) until the buffer properties
  dialog was shown at least once.

Version 3.0.5 - 8/9/2012
* Fixed bug with datagrid click when serching stanalone tables.
* Fixed bug with dropdownlist in multi field expressions not initializing
  properly on startup and on layer change.

Version 3.0.4 - 8/8/2012
* Fixed a few more bugs with datagrid hovering and datagrid field formatting.

Version 3.0.3 - 8/7/2012
* Fixed a few bugs with datagrid and no results from a search.

Version 3.0.2 - 8/3/2012

* Added the ability to have a grid hyperlink icon instead of only hyper link text. This is achieved through
  the new hyperlinkgridicon attribute of a field element.
* Added a new option to the graphical search page that allow you to include the text search options to the
  graphical search if the search layer dropdown is the same on both pages.
* The buffer graphics have a new popup GUI for adjusting their graphics symbology.
* The userlist attribute have a new ability, when you add the text "all" to the comma separated userlist
  and the user chooses this value, then all the values of the userlist will be selected when the query is
  executed.
* All possible items in code have been migrated from mx to spark (probably doesn't mean much to you as the 
  end user, but for me as the developer, it allowed to enhancement to be accomplished).

Version 3.0.1 - 7/26/2012

* The name of the swf and xml file has changed to eSearchWidget.swf and eSearchWidget.xml
* Fixed application hang bug when using the eSearch and new 3.0 print widget.
* Added autozoom configuration to zoom to the selected features automatically whena search is complete.
* Added keepgraphicalsearchenabled configuration option to keep the graphical selection tool that the 
  user chooses active even after a selection has been made. This means that you will not have to clear 
  your selection and re-choose a graphical selection tool in order to make another selection.
* Added autohide to the fixed datagrid. Control of this is now in the SearchWidgetFixedDG.xml file.
* Added predefined datagrid column sorting to all the datagrids. 

Version 3.0 - 6/13/2012
* Recompiled for Flex Viewer 3.0
* Fixed issue this tables and new link style

Version 2.9.0 - 6/5/2012
* Added multi-field search expression capability.
* Added attachment support for popups.
* Added multi-field hyperlinks capability.
* When URL Search is performed the GUI reflects the that search criteria.
* Fixed an issue with open SQL URL searches.
* Added link icon tooltip.
* Fixed issue with relate fixed datagrid hyperlinks.
* Fixed issue with interaction with point buffer widget.

Version 2.5.1.7 - 4/19/2012
* Added ability to search (flat/standalone/no geometry) tables.
* This time all Zooming uses the same scaling (popup, datagrid, widget results, zoom to all).
* Added Relates icon/button to datagrids so that you can click on it in the datagrid to
  open relates choice dialog.
* Move all skins to a skins package for cleaner organization.
* Links that are not associated with a field now work.
* Ability to disable the relates tab in the fixed widget is now configurable.

Version 2.5.1.6 - 3/19/2012
* Fixed more issues with subtypes in the datagrids.
* Added new zoom percent to the zoomscale tag where 1 = 100%, 1.2 = 120% (default), etc, etc.
* All Zooming attempts to use the same scaling (popup, datagrid, widget results).
See ReadMe.txt for a complete list of updates.

Version 2.5.1.5 - 3/16/2012
* Fix more issues with subtypes and a possible issue with integer fields.

Version 2.5.1.4f - 2/24/2012
* Fix error 1009 that was recieved in version 2.5.1.4 when no relate was specified in the XML for a layer.

Version 2.5.1.4 - 2/22/2012
* Each relate can have their own associated icon now.

Version 2.5.1.3 - 2/21/2012
* Fixed issue where you could no longer use an open SQL expression because single quotes
  where being automatically escaped.
* Fixed issue with event theme layers used in a search not having an ObjectID or FID field
  and thus causing the datagrid/results interaction to fail

Version 2.5.1.2 - 1/12/2012
* Fixed error that occurs when you are using the floating adatgrid and click clear,
  then close the datagrid and reopen it the data reappears in the grid and hovering
  over arecord causes an error.

Version 2.5.1.1 - 1/11/2012
* Added the ability to disable the interaction between the widget results and the datagrids
  This becomes important when you have more than 500 results displayed in the datagrids
  Thanks to Dave Jenkins for this suggestion
* Fixed error what occurred when the search widget was minimized and you hover over a grid result
* Added ability to disable the datagrid in the disablebuttons element

Version 2.5.1 - 1/10/2012
* Added the ability to buffer graphics drawn using the graphical search before the 
graphical search is performed.

Version 2.5.0.10 - 1/6/2012
* If you have multiple links that contain images then the popup will now display all the images
in the popup media browser
* If a link returns the text "unavailable" than the link will not be added to the widget results,
popup or either of the datagrids hyperlink results.


Version 2.5.0.9 - 1/6/2012
* Fixed more issues with new multiple links code only grabing link from first 
record and using that for all results.

Version 2.5.0.8 - 12/30/2011
* Fixed issue with new multiple links not displaying a link in the widgets 
  results if only on link is specified.
* Fixed error when fields all="true" is used in version 2.5.0.7 all the fields 
  contain the name and data of the last field.

Version 2.5.0.7 - 12/27/2011
* Fixed issue with datagrids when compiled using the Adobe 4.5.1 SDK
* Added Multiple Link Support.

Version 2.5.0.6 - 12/21/2011
* Fixed issue where in some circumstances the Fixed Data Grid could 
  extent past the applications width.

Version 2.5.0.5 - 12/8/2011
* Fixed relates button not showing up unless you first do a text search.
* re-enabled the polygon and polyline graphical search abilities.
* When "enable multi-part graphics" is selected and then the Search button is pushed 
  the graphical searches draw tool is now turned off. Meaning after you click search 
  you will have to choose a search geometry type button to perform another search.
* If using the Fixed Datagrid and a relate is chosen then the relate tab is activated. 

Version 2.5.0.4 - 12/7/2011
* Fixed a relate query error that only ocurred in certain situations

Version 2.5.0.3 - 12/6/2011
* Fixed Coded domains bug introduced in version 2.5.0.1
* Relates Sum field does not clear when choosing a relate that has no sum field
  specified.

Version 2.5.0.2 - 12/5/2011
* Depreciated tolerance. Now just use toleranceforpointgraphicalselection
* Added a tolerancebydefault option to the SearchWidget.xml.

Version 2.5.0.1 - 12/5/2011
  * Fixes bug where subtype was not displayed correctly in the 2 datagrid types.

Version 2.5 - 12/2/2011
  * Added Related table display capabilities for searched features
  * Added support for domains that come from subtypes.

Version 2.4.0.14 - 11/19/2011
  * Grid auto sizes to the hyperlink alias if that length is smaller than the column header
  * Fixed issues with alias not getting set for hyperlinkalias if the column name alias was
    not also specified or the case did not match.

Version 2.4.0.13 - 11/2/2011
  * Fixed issue with using existing buffer point and use existing draw graphic not enabling
    unless the eSearch is open before the graphics of those widgets were drawn.
  * If you select a graphical draw tool and do not draw a graphic and then switch to text search
    the draw tool is still active and tooltip is displayed. This has been fixed to disable the 
    draw tool when switching away from the graphical search view.
  * When closing the widget if a buffer graphic is on the screen it's graphics layer will be 
    hidden like the other graphics layers

Version 2.4.0.12 - 10/25/2011
  * Repaired the Fixed Datagrid to display coded values when fields have domains. There was a bug
    when you first executed the search the coded values where not displayed but subsequent queries
    would work.

Version 2.4.0.11 - 10/13/2011
  * Fix datagrid autosize function when using mapservices with joins 
    in both the floating and fixed datagrids

Version 2.4.0.10 - 09/13/2011
  * linkaliastext not being honored when left clicking graphic.
  * ItemRollOut in data grid no longer automatically closes the info popup for that graphic.

Version 2.4.0.9 - 09/12/2011
  * Added ability to specify linkaliastext for standard linkfield

Version 2.4.0.8 - 09/10/2011
  * URL Searches that return single geometry now zoom to return geometry properly.

Version 2.4.0.7 - 09/03/2011
  * Null values are now empty strings when exported as csv or txt from the datagrid.
  * Added support for Range domains to be used and user entry validated against that
    Range domains min and max values.

Version 2.4.0.6 - 08/19/2011
  * Fixed Issue with buffer point widget and enhanced draw widget buttons displaying as disabled
    even when they should have been enabled.

Version 2.4.0.5 - 08/18/2011
  * Fixed Issue with fixed datagrid not populating when using the URL Query
  * Fixed some grammatical errors
  * Fixed issue with zoom to and clear not showing when using the URL Query

Version 2.4.0.4 - 08/16/2011
  * Fixed Issue with datagrid not automatically retrieving the grid field alias for Hyperlinkfields.
  * Fixed Issue with changing enablemultipartsearch in xml did not have any effect in widget.

Version 2.4.0.3 - 08/15/2011
  * datagrids now honor the useutc attribute of a date field.
  * Removed leftover alert window when using a link field.

Version 2.4.0.2 - 08/05/2011
  * Added the useutc attribute to the field element to allow the utc offset to be aplied to dates

Version 2.4 - 07/27/2011
  * Both the compiled and uncompiled version can use the URL Search capability.
    See the Enhanced Search Widget URL Search Configuration.pdf
  * Links in the results, popUp and Data grid now do not display a link if the link field contains
    a Null or empty string.
  * Fixed error when clearing the graphics results and using the fixed data grid.
  * Fixed issue with buffer point widget button displaying as enabled after you hover over it, even
    though it is not enabled.

Version 2.3.4 - 07/19/2011
  * Added a child widget that allows you to have a fixed postion datagrid instead of the floating datagrid.
  * Added the Enhanced Search Widget Fixed Datagrid Setup.pdf to help with the setup.

Version 2.3.3 - 07/15/2011
  * Added option to use existing Point Buffer Widget graphics when doing graphical selection.

Version 2.3.2.5 - 07/08/2011
  * Added option to zoom to all returned results.

Version 2.3.2.4 - 06/24/2011
  * Added option to enable or disable the new Multi-part geometry graphical search in the config (for startup) and on
    the user interface (for runtime change).

Version 2.3.2.3 - 06/24/2011
  * Added new ability to do muti part geometry graphical searches. What this means is the graphical search
    is no longer executed immediately after you draw on the map you can draw multiple same geometry types
    and then click the new search button on the graphical search dialog and the search will be preformed
    using all the drawn geometries. Thanks to Nathan Enge for encouraging me to look into this enhancement
    again.
  * Better interaction has been established with the eDraw widget and the button to use the existing eDraw
    graphics is enabled or disabled based on the presence of eDraw graphics layer and number of graphics.
    There can now be multiple eDraw graphics on the screen for the search to use if they are similar geometry
    types.
  * Fixed the graphical search tool not deactivating. It deactivates now when you click clear.
  * Fixed the selectedgraphicaltool option not activating correctly.

Version 2.3.2.2 - 06/24/2011
  * Added new ability to do muti part geometry graphical searches. What this means is the graphical search
    is no longer executed immediately after you draw on the map you can draw multiple same geometry types
    and then click the new search button on the graphical search dialog and the search will be preformed
    using all the drawn geometries. Thanks to Nathan Enge for encouraging me to look into this enhancement
    again.
  * Better interaction has been established with the eDraw widget and the button to use the existing eDraw
    graphics is enabled or disabled based on the presence of eDraw graphics layer and number of graphics.
    There can now be multiple eDraw graphics on the screen for the search to use if they are similar geometry
    types.

Version 2.3.2.1 - 06/23/2011
  * Added new option "selectedgraphicaltool" for allowing a particular graphical search tool to be selected
    uppon widget load if the defaultselectionoption = graphicalInput. 

Version 2.3.2 - 05/22/2011
  * Option added to each layer for opening the datagrid automatically when a search is executed.
  * usegeometry attribute added to the zoomscale element to specify if the geometry or the scale will be
    used in the zoom when a record is clicked.

Version 2.3.1 - 05/02/2011
  * Better Spatial Search results and performance
  * Fixed image in popup not showing

Version 2.3 - 04/25/2011
  * This version is only for FlexViewer 2.3
  * Uses new Flex API Popup Windows
  * Added definition Query Support to xml configuration.
  * Added user lists. This for people who want to specify certain values that will appear in a dropdown
    instead of having the user type the search string. (comma separated list)
  * Enhanced URL Search 
       - Now allows for specifying the layer and expression to search
       - Now the ability to have the datagrid opened from the url search automatically.
  * Compiled widgets for older viewer versions are now no longer provided. (Time to move on people).
  * Many code changes to parallel the standards and practices that esri are putting in their widgets.

Version 2.2.11 - 03/15/2011
  * Fixed showing the datagrid after performing a search from the Flex Viewers URL
    !!!!!!Requires Mods to several Flex Viewer components, See additional instructions!!!!!!
  * Enhanced Search Widget URL Search Configuration.pdf has been update for some oversights and omissions.

Version 2.2.10 - 03/4/2011
  * Fixed the graphical search ability to specify a sum field.
  * Added support for performing a search from the Flex Viewers URL
  !!!!!!Requires Mods to several Flex Viewer components, See additional instructions!!!!!! 

Version 2.2.9 - 02/24/2011
  * Added the ability to specify a sum field. It is your responsibility to only specify sum for one field 
    per layer, to only specify sum on a numeric field, and it must be a grid field!
  * Fixed a bug with the fields all="true".

Version 2.2.8 - 02/14/2011
  * Added the ability to disable the graphical search using existing draw/eDraw widget graphics.
  * Change made when there is not Spatial Relation operations specified in the config file there
    Will be no combobox and label presented on the spatial search page, just the buffer options.

Version 2.2.7f - 02/08/2011
  * Added the ability to resize the floating data grid.
  * Fixed an issue with disable/enable export option in the data grid on a layer by layer basis.
  * Fixed issue with symbology alpha and color being set to 0 or 0x000000.
  * Added ability to define a simple marker symbol for point or the current picture marker symbol.
  * Fixed SearchWidget.xml issue

Version 2.2.6 - 02/01/2011
  * Added the ability to disable/enable export option in the data grid on a layer by layer basis.
  * Fixed issue with sorting data grid columns when layer has a join
  * Fixed issue with tooltips hanging for coded value domain combobox when using mouse wheel.
  * Changed packaging of widget so that assets are included in widget folder for
    easier moving of widget to new versions of the Flex Viewer.

Version 2.2.5 - 01/19/2011
  * Added the ability to use coded value domain values in a combobox instead of typing in a text input box.
  * Added configuration option to disable certain titlebar buttons.
  * Added configuration option to set the default search option on widget load i.e. text, graphical, or spatial
  * Added configuration option to add a pixel tolerance to the graphical point search for point on point searches.

Version 2.2.4 - 01/13/2011
  * Fixed Issue with existing draw graphics working for the graphical search.

Version 2.2.3 - 01/06/2011
  * Fixed Issue with all spatial button firing intersects instead of what they were intended to fire
  * Added a clear text button to the results page.
  * Better Spatial Icons

Version 2.2.2 - 12/29/2010
  * Fix issue with this 2.2.1 spatial query not honoring configuration info.
  * Added icons for other supported spatial searches.
  * depreciated the use of esriSpatialRelRelation.

Version 2.2.1
  * Fixed the issue of the color picker and alpha slider not worker for the buffer.
  * Rearranged the graphics layer order to put the buffer under the selected feature.
  * Adjusted the SearchWidget.xml so that miles are not the default in the spatial search.
  * Fixed issue with hyperlink grid field optional attributes like hyperlinkaliastext, linkprefix, 
    and linksuffix in this version you can omit hyperlinkaliastext, linkprefix, and linksuffix or 
    set them to = "" and it not have an adverse effect as in versions prior to 2.2.1

Version 2.2
  * Added compiled versions for FlexViewer 2.1 and 2.2
  * REALLY Fixed Issue with linkprefix in datagrid not getting cleared when new search results are issued.
  * Completely reworked the way Spatial Searches are done (Thanks to Erwan).
  * Added ability for layer to have multiple different SQL Expressions.
  * Added Export to tab delimited text as well as comma separated value.

Version 2.1.7
  * Fixed Issue with linkprefix in datagrid not getting cleared when new search results are issued.

Version 2.1.6
  * Fixed Issue with spatial search requiring the use of a buffer.
  * Other minor spatial search tweaks like "where" checkbox tooltip displays example for where clause.
  * Fixed Graphical search indicating it is selected when widget is first shown even know it is text
  * Spatialreference that is specified in the xml is now used for the buffers spatialrefernce

Version 2.1.5
  * Fixed Issue with graphical search not working when spatialsearchlayer and/or spatialrelationlayer
    was set to true for a layer. Thanks to Jos Vroegop for finding this.

Version 2.1.4
  * Enhancement made to return coded values if a field has a coded value domain
  * Fixed Issue with DataGrid not using linkprefix and linksuffix if specified

Version 2.1.3
  * Enhancement made to allow csvSeparator and export button label to be specified for non U.S. users
  * Enhancement made to allow for linkprefix text to be added in front of the linkfield
    and linksuffix text to be added to the end of the linkfield
  * Enhancement made to allow link iconfield to be specified as well as iconprefix and iconsuffix
  * Spatial Search where clauses can now use the already specified query expression or (the Default) use
    a fully user specified where clause.
  * Fixed issue with hyperlink field showing alias(undesired) when exported to CSV if an alias is specified.

Version 2.1.2
  * Enhancement made to allow fields to have numeric or currency formatting
  * Fixed issue with datagrid opening even without grid fields defined - Thanks to Alex Jones for this fix
  * Fixed bug introduced by v2.1.1 where hyperlink columns not showing in datagrid

Version 2.1.1
 * Fixes issue with Search Results not have all the specified fields
 * Enhancement made to use fields alias if an alias is not specified in the SearchWidget.xml
 * Enhancement made to use the dateformat attribute in the datagrid for date fields also
 * Fixed integration issue with the draw widget
 * Fixed the issue of the graphics not be clear from the screen when the widget is closed

Version 2.1

*Enhancement and migration to FlexViwer 2.1
- You now have the ability to do a spatial search such as select traffic cameras
  that are intersected by a buffer of 400 Meters on land zoning polygons with a 
  Zoning_code = 'R1'  

*******************************************************************************
****    Thanks to Erwan Caradec for contributing this code addition        ****
*******************************************************************************
- Skins have been developed for several of the floating Data grids components.
- Field specification has been simplified you now specify the field you want and
  give then attributes of whether or not they show up in the grid exclusively, 
  are hyperlinks, their alias, etc. The SearchWidget.xml has details of each 
  attribute used.

Version 1.07
*Enhancement
- You will now be able to search using existing graphics from the Draw Widget
- You need to make a modification to the Draw Widget for this to work (See below in
How to install section).

Version 1.06
*Bug Fix:
- Fixed issue with populating Datagrid fields if datagrid is already open
- Removed dependency on having InfoPopup.mxml and RecordData.mxml modified.

Version 1.05
*Bug Fix:
- Fix issue with Datagrid dataGridColumn label treating a joined field as dot notation instead of
  and actual field name.

version 1.04
 - Fix compile bug introduced in 1.0.3

version 1.03
 - Now supports field aliases for datagrid column headers
 - Now supports html text in the content results
   * on line 527 of the SearchWidget.mxml just change <font color='#FFFF00'> which is yellow to your desired font color
 - Now supports individual layer zoom scales

version 1.01
 - Export DataGrid Results to CSV (Requires 3.2 SDK and Flash Player 10.0.22 or higher)
 - Ability to have the hyperlink field show the url or an alias of "Get Hyperlink" in the datagrid.
   

## Features

    This sample provides an enhanced version of the SearchWidget for the Flex Sample Viewer.
This enhanced version allows you to open a datagrid from the SearchWidget that has its own
specified fields that are independent of the fields that are specified for the SearchWidget.
The DataGrid is also an enhanced DatGrid that automatically resizes the columns to fit the data
inside of them and also for hyperlink fields to be specified. The DataGrid is fully integrated 
with the SearchWidgets results so when you select a row in the datagrid the same record is 
selected in the SearchWidgets results and vice versa. The DataGrid is in a floating container 
so it can be moved to anywhere on the screen, but is not resizable.

    The intention of this enhancement is to allow a minimal amount of attributes to be displayed
in the standard SerachWidget's results and info window and also allow for detailed or numerous 
attributes to be displayed when the user what more information.


What's in the zip file:

ExportButtonSkin.mxml  	- This is a simple skin to allow the display of a good graphic on a button with text.
HyperLinkColumn.mxml        	- Allows for the Datagrid to have a field that contains a url to function as a hyperlink.
SearchResult.as			- This is basically the attributes of the search results.
SearchResultDatagroup.as	- This is the event dispatcher for the search results.
SearchResultItemRenderer.mxml	- This is the item renederer for the Spark data group that displays the search results.
SearchWidget.mxml  		- Standard ESRI SearchWidget Enchanced to add the floating DataGrid and interaction between results and DataGrid, 
				  and remove Shape_Length, Shape_Area fields from the results.
SearchWidget.xml                - Standard ESRI SearchWidget configuration file with many additions to configure the enhanced features of this widget.
SearchWidgetFloatDG.mxml        - A customized datagrid that automatically resizes the columns to fit the data and is in a floating canvas.
SearchWidgetFloatDGSkin.mxml    - This is a skin that allows the use of the export button skin and the close widget button skin on the form.
WidgetCloseButtonSkin.mxml	- I created this skin so that it would not be necessary to create a png for the close button that matched the 
				  current theme	being used.
i_table2.png			- a icon file for the button that brings up the floating DataGrid
i_searchspatial.png		- a icon for the spatial search.
i_draw_draw.png			- a icon for the use of the draw widgets graphics


## Requirements
- The ArcGIS Flex API 2.x or greater swc. Download it here:  http://resources.esri.com/arcgisserver/apis/flex/index.cfm?fa=downloadDisclaimer
- Internet access to the ArcGIS Online servers
- Web Server to deploy the application
- Flash Player 10

## How to install


**********************************************************************************
** IMPORTANT FOR the use of existing draw graphics to be used for the graphical **
** search you need to follow the next step below                                **
**********************************************************************************
 - Add the following lines to the DrawWidget.mxml in the init function under this line 'graphicsLayer = new GraphicsLayer();'
	graphicsLayer.name = "Draw Features";
	graphicsLayer.id = "Draw Features";


For both the compiled and uncompiled version you need to copy the contents
of the assest/images to your projects assets/images folder.

To install using the compiled version just copy the folder called eSearch
under the Widgets folder, and add this line to your config.xml

<widget label="Enhanced Search" left="60" top="400"
                icon="assets/images/i_search.png"
                config="widgets/eSearch/SearchWidget.xml"
                url="widgets/eSearch/SearchWidget.swf"/>

For the Uncompiled you need to copy the eSearch folder to src/widgets

Finalize the install for Uncompiled version:
 - In Flex Builder on the left of the screen is the FlexNavigator tree, right click you Flex Sample Viewer project
   and go to properties
 - In the Properties dialog choose Flex Compiler in the left window.
 - Ensure your Flex SDK Version is 4.0
 - Check Require Flash Player Version under HTML Wrapper and enter 10.0
 - Now Flex Modules in the left window.
 - On the right hand side of the dialog will be an add buton click it
 - browse to src\widgets\eSearch and add the SearchWidget.mxml
 - click ok all the way out.
 - Change the SearchWidget.xml just like you would in the original SearchWidget that ESRI provided and add your gridfields
   and gridhyperfields (these are optional if you do not want a datagrid for a particular layer then just leave these
   elements empty.

That�s it enjoy, if you have any comments or suggestions just post a comment on the code gallery.

Robert Scheitlin
GIS Manager
GIS Programmer
Calhoun County Commission
Alabama
