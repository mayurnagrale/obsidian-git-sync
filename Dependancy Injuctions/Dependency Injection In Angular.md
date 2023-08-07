user.service.ts
import Injectable from Angular/Core

export class userService{
	private username: string = 'JohnDoe';

  getUsername(): string {
    return this.username;
  }
}

// user-profile.component.ts

import { Component } from '@angular/core';
import { UserService } from './user.service';

@Component({
  selector: 'app-user-profile',
  template: '<p>User Profile: {{ username }}</p>'
})
export class UserProfileComponent {
  username: string;

  constructor(private userService: UserService) {
    this.username = this.userService.getUsername();
  }
}

mention userservice in AppModule file in providers

// app.module.ts

import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { UserProfileComponent } from './user-profile.component';
import { UserService } from './user.service';

@NgModule({
  declarations: [UserProfileComponent],
  imports: [BrowserModule],
  providers: [UserService],
  bootstrap: [UserProfileComponent]
})
export class AppModule {}