---
uid: 10_1_0_Cube_RNs
---

# DataMiner Cube 10.1.0 release notes

> [!IMPORTANT]
> We are still working on this release. Some release notes may still be modified or moved to a later release. Check back soon for updates!

## Changes in DataMiner 10.1.0 CU18

### Enhancements

#### Alarm Console: Time of history sets will now always be converted to the local time zone [ID_33849]

<!-- Main Release Version 10.1.0 [CU18]/10.2.0 [CU6] - Feature Release Version 10.2.9 -->

From now on, the time of history sets will always be converted to the local time zone.

#### Alarm Console: A run-time error will now appear when the Resource Manager failed to initialize [ID_34024]

<!-- Main Release Version 10.1.0 [CU18]/10.2.0 [CU6] - Feature Release Version 10.2.9 -->

From now on, the following run-time error will appear in the Alarm Console when the Resource Manager failed to initialized.

```txt
An unexpected exception has occurred while initializing Resource Manager. Please check the SLResourceManager logging for more information.
```

### Fixes

#### Trending: Creation, update and deletion of a trend pattern would not be communicated to the other DataMiner Agents in the DMS [ID_33624]

<!-- Main Release Version 10.1.0 [CU18]/10.2.0 [CU5] - Feature Release Version 10.2.8 -->

When you created, updated or deleted a tag, up to now, this would incorrectly not be communicated to the other DataMiner Agents in the DMS.

#### SLAnalytics - Pattern matching: No 'suggestion event' type alarm would be triggered in case of DVE elements [ID_32671]

<!-- Main Release Version 10.1.0 [CU18]/10.2.0 [CU6] - Feature Release Version 10.2.5 -->

From DataMiner 10.0.13 onwards, you can activate alarm monitoring of trend patterns, so that a "suggestion event" type alarm is triggered whenever a specific pattern is detected. In case of dynamic virtual elements, in some cases, no "suggestion event" type alarm would be triggered.

#### Alarm Console would incorrectly keep loading while the tickets linked to the alarms were being loaded [ID_33847]

<!-- Main Release Version 10.1.0 [CU18]/10.2.0 [CU6] - Feature Release Version 10.2.9 -->

When you open DataMiner Cube, it will load the alarms and try to link the existing tickets to them so it can show the ticket information in the Alarm Console.

While this process was ongoing, in some rare cases, the Alarm Console would incorrectly keep on loading.

#### Alarm Console: Problem when loading [ID_33860]

<!-- Main Release Version 10.1.0 [CU18]/10.2.0 [CU6] - Feature Release Version 10.2.9 -->

In some cases, an exception could be thrown while the Alarm Console was loading.

#### Alarm Console: Cube could become unresponsive when a large number of alarms were being added and removed in an alarm tab of type 'sliding window' [ID_33870]

<!-- Main Release Version 10.1.0 [CU18]/10.2.0 [CU6] - Feature Release Version 10.2.9 -->

When, in an alarm tab of type "sliding window", a large number of alarms were being added and removed, in some cases, DataMiner Cube could become unresponsive.

#### System Center: Element counter on Agents > Status tab would not be set to 0 when removing all elements from a DMA [ID_33885]

<!-- Main Release Version 10.1.0 [CU18]/10.2.0 [CU6] - Feature Release Version 10.2.9 -->

When you go to *System Center > Agents > Status*, the *Elements* column shows you how many elements are being hosted by each agent in the DMS.

When, on a particular agent, you removed all elements, the number of elements of that agent would incorrectly not be set to 0. Instead, it would be set to the last-known number of elements on that agent before the element were removed.

#### Alarm Console: Column list not shown when hovering over the 'Add/Remove column' menu command [ID_33967]

<!-- Main Release Version 10.1.0 [CU18]/10.2.0 [CU6] - Feature Release Version 10.2.9 -->

When you right-clicked a column header in an alarm tab and hovered over the *Add/Remove column* command, in some cases, the column list would incorrectly not be shown if, previously, you had right-clicked the header of the focus column or a header of an action column.

#### Data Display : Update of parameter unit would not be reflected in the UI when the element card was open [ID_34007]

<!-- Main Release Version 10.1.0 [CU18]/10.2.0 [CU6] - Feature Release Version 10.2.9 -->

When an element card was open on the DATA page, and a parameter on that page had its unit changed (e.g. via an Automation script), that change would incorrectly not be reflected in the UI. To see the new unit, you had to close the element card and re-open it.
