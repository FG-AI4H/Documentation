# Summary
The Free Software initiative started in its current structure in September 2020 and leverages all the work accomplished by the FG-AI4H since 2018.

## Milestones
::: mermaid
gantt
    dateFormat  DD-MM-YYYY
    title       Free Software MVP Phase
    excludes    weekends
    

    section Infrastructure
    Completed task            :done,    des1, 01-12-2020,14-12-2020
    Active task               :active,  des2, 01-12-2020, 3d
    Future task               :         des3, after des2, 5d
    Future task2              :         des4, after des3, 5d

    section Data Acquisition
    Completed task in the critical line :crit, done, 01-12-2020,24h
    Implement parser and jison          :crit, done, after des1, 2d
    Create tests for parser             :crit, active, 3d
    Future task in critical line        :crit, 5d
    Create tests for renderer           :2d
    Add to mermaid                      :1d

    section Data Storage
    Describe gantt syntax               :active, a1, after des1, 3d
    Add gantt diagram to demo page      :after a1  , 20h
    Add another diagram to demo page    :doc1, after a1  , 48h

    section Evaluation
    Describe gantt syntax               :after doc1, 3d
    Add gantt diagram to demo page      :20h
    Add another diagram to demo page    :48h

    section Reporting
    Describe gantt syntax               :after doc1, 3d
    Add gantt diagram to demo page      :20h
    Add another diagram to demo page    :48h
:::

