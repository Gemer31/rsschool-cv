## Roman Kravchenko

---

### Contact information:

|     Phone     |         E-mail            |           LinkedIn         |           Discord          |
|:-------------:|:-------------------------:|:--------------------------:|:--------------------------:|
| +375298023316 | romakravcenko31@gmail.com | roman-kravchenko-40b845250 | Roman Kravchenko(@Gemer31) |

---

### About Myself:
Open to learning new technologies! I'm interested in everything related to JS/TS and want to know front-end in details.

---

###  Skills:
* HTML | CSS
* JavaScript | Typescript
* Angular | Vue
* RxJS | Vuex

---

###  Work Experience:
**Front-end developer**: Netcracker (08-2019 - Present) <br>
Stack: *Angular*, *TS*, *JS*, *NgRx*, *Less*, *Apollo*, *TextCafe*

---

### Code example:
Recursive function for delete elements from object
```ts
export function deleteObjElements(deletedElements: DeletedElement[], obj: unknown, objName?: string): void {
    deletedElements.forEach((deletedElement: DeletedElement) => {
        if (Array.isArray(obj)) {
            obj.forEach((nextObj: unknown) => deleteObjElements(deletedElements, nextObj, objName));
        } else {
            if (obj && typeof obj === "object") {
                if (!deletedElement.objName
                    || deletedElement.objName === objName
                    || (deletedElement.objName === "root" && !objName)) {
                    delete obj?.[deletedElement.element];
                }
                Object.entries(obj).forEach(([nextObjName, nextObj]: [string, unknown]) =>
                    deleteObjElements(deletedElements, nextObj, nextObjName),
                );
            }
        }
    });
}
```

Example:
```ts
deleteObjElements(
    [
        {element: "__typename"},
        {objName: "root", element: "id"},
        {objName: "languages", element: "typescript"},
    ],
    input,
);
```

Input:
```json
{
  "id": "1",
  "firstName": "firstName",
  "lastName": "lastName",
  "languages": {
    "javascript": true,
    "typescript": false,
    "__typename": "languages"
  },
  "__typename": "programmer"
}
```

Output:
```json
{
  "firstName": "firstName",
  "lastName": "lastName",
  "languages": {
    "javascript": true
  }
}
```

---

### Trainings and Courses:
**Skillbox**
* Framework Vue.js (finished)
* Project internship Vue.js (finished)
* Framework React.js (in progress)

**RSSchool**
* JavaScript/Front-end 2023Q1 (in progress)

---

### Languages:
* Russian (Native)
* English (B1)

---

### Education
Belarusian State University of Informatics and Radioelectronics(BSUIR)
   