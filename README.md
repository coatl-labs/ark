# Qoatl/Ark

### Description

Ark is a simple and fast JSON object storage system written in Typescript with a focus on simplicity and performance for persistence of information stored in the file system.


```ts
import { Ark } from '@qoatl/ark';

interface User {
  name: string;
  age: number;
}

const db = new Ark<Ark[]>('users');

await db.connect();

db.set('1', { name: 'John Doe', age: 30 });

await db.save();
```