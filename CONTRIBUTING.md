# CONTRIBUTING: Notes on forks and pull requests

We are thrilled that you would like to collaborate on 
this project. Your help is essential.


## Submitting a pull request

0. [Fork][fork] and clone the repository.
0. Create a new branch: `git checkout -b my-branch-name`
0. Make your change, add tests, and make sure the tests still pass.
0. Push to your fork and [submit a pull request][pr]
0. Wait for your pull request to be reviewed.


## Testing

Tests are contained within the module itself. 
The default database file db0 assigned in class Base presumes 
Linux top directory /tmp (change to suit your system) -- 
yserial is designed to operate *cross-platform* including Windows.

```py
     import y_serial_dev as y_serial
     y_serial.tester()
     #        ^for the principal class Main
     #        testfarm is for the beta version, not yet in Main.
     #   Flip the DEBUG variable for verbose results. 
```


## Tips regarding pull requests

- Refine the tests whenever possible.

- Update documentation as necessary.  

- Keep your change focused. If there are multiple changes that are not
  dependent upon each other, please submit them as separate pull requests.

- Write a [good commit message](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html).

Thanks very much for your consideration. Looking forward to reviewing your
code.


## Resources

- [Contributing to Open Source on GitHub](https://guides.github.com/activities/contributing-to-open-source/)
- [Using Pull Requests](https://help.github.com/articles/using-pull-requests/)


[fork]: https://github.com/rsvp/yserial/fork
[pr]: https://github.com/rsvp/yserial/compare
