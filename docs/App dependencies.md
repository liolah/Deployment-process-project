# App dependencies
### Frontend app dependencies
- The frontend is built using Angular framework and Ionic. 
- Unit tests and e2e tests are done using jasmine. Test results are delivered using karma.
- The app is made with typescript. tslint and ts-node are also used with ts.

#### - Production dependencies
- All dependencies can be found in details in the project is package.json, however, in brief, the dependencies are:
   - Angular 
   - Ionic 
   - core-js
   - rxjs
   - zone.js
#### - Development dependencies
- The dev dependencies used in the frontend are:
    - Typescript 
    - tslint
    - ts-node
    - Jasmine
    - Karma
    - Codelyzer

### Backend app dependencies
- The backend is built using express and uses a postgres database. Additionally, it's cors enabled and uses JWTs.
#### - Production dependencies
- aws-sdk
- bcrypt (for passwords hashing and encryption)
- cors
- dotenv
- express
- jsonwebtoken
- pg
- sequelize
#### - Development dependencies
- Typescript, with type definitions for all production dependencies
- chai
- eslint
- mocha
- ts-node
