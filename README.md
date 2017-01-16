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

@Component({
    selector: 'simple-chart-example',
    template: `
        <chart [options]="options"></chart>
    `
})
export class App {
    constructor() {
        this.options = {
            title : { text : 'simple chart' },
            series: [{
                data: [29.9, 71.5, 106.4, 129.2],
            }]
        };
    }
    options: Object;
}
```