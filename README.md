#Angular 2 Gantt Chart Component 

#### Setup App Module
```TypeScript
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { GanttModule } from 'angular2-ganttchart';
import { App } from './App';

@NgModule({
    imports: [BrowserModule, GanttModule],
    declarations: [App],
    bootstrap: [App]
})
export class AppModule {}
```
#### Create First Gantt Chart Component
Main charts functionality provided by the `chart` component and its `options` property.

```TypeScript
import { Component } from '@angular/core';
import {Gantt} from 'angular2-ganttchart'
@Component({
    selector: 'simple-gantt chart-example',
    template: `
        <gantt-chart [gantt]="gantt"></gantt-chart>
    `
})
export class App {
    constructor() {
        // StartDate
        // EndDate
        // ActualStartDate
        // ActualEndDate
        // ForcastedDate
        //Progress
        //Status
        //Gantt direction 
        this.gantt = new Gantt("01/01/2016", "11/30/2016", "01/20/2016", "11/15/2016", "", 100, 3,false);
    }
    gantt: Gantt;
}
```