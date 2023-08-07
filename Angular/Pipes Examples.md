1. **Using the `DatePipe`**: 
    import { Component } from '@angular/core';
@Component({
  selector: 'app-root',
  template: `
    <h2>Date Pipe Example</h2>
    <p>Original Date: {{ originalDate }}</p>
    <p>Formatted Date: {{ originalDate | date:'dd/MM/yyyy' }}</p>`
})
export class AppComponent {
  originalDate: Date = new Date();
}


2.  **Using the `UpperCasePipe`**:
 import { Component } from '@angular/core';
@Component({
  selector: 'app-root',
  template: `
    <h2>UpperCase Pipe Example</h2>
    <p>Original Text: {{ originalText }}</p>
    <p>Uppercase Text: {{ originalText | uppercase }}</p> `
})
export class AppComponent {
  originalText: string = 'Angular Pipes Example';
}

3. 
