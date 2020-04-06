# Angular Project EP1 : LOGIN & REGISTER

## Boostrap Import
#### index.html
```bash
    <!-- Main CSS-->
    <link rel="stylesheet" type="text/css" href="assets/css/main.css" />
    <!-- Font-icon css-->
    <link
      rel="stylesheet"
      type="text/css"
      href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css"
    />
  </head>
  <body>
    <app-root></app-root>
    <!-- Essential javascripts for application to work-->
    <script src="assets/js/jquery-3.2.1.min.js"></script>
    <script src="assets/js/popper.min.js"></script>
    <script src="assets/js/bootstrap.min.js"></script>
    <script src="assets/js/main.js"></script>
    <!-- The javascript plugin to display page loading on top-->
    <script src="assets/js/plugins/pace.min.js"></script>
  </body>
```

## Routing File
#### 'app.url.ts
```bash 
export const AppURL = {
    Login: 'login',
    Register: 'register',
    Authen: 'authentication'
}
```
#### 'app.routing.ts'
```bash 
import {Routes, RouterModule} from '@angular/router'
import { AppURL } from './app.url'
import { LoginComponent } from './components/login/login.component'
import { RegisterComponent } from './components/register/register.component'

const RouteLists:Routes = [
    { path:AppURL.Login, component: LoginComponent},
    { path:AppURL.Register, component: RegisterComponent}
]
export const AppRouting = RouterModule.forRoot(RouteLists)
```	

#### 'app.module.ts'
```bash
    imports: [AppRouting]
```

## Login & Register Component

#### NPM INSTALL
```bash
$ ng generate component login
```
#### 'login.component.css'
```bash
.login-box{
    min-height: 420px;
    margin-bottom: 15px;
}
```
#### 'login.component.ts'
```bash
import { AppURL } from '../../app.url'
```
```bash
export class LoginComponent implements OnInit {
  Url = AppURL;
}
```
#### 'login.component.html'
```bash
  <a [routerLink]="['/',Url.Register]">SIGN UP</a>
```
