# Xss and Authorization

# Xss & Authorization

**Reflected Xss** – The user input goes to the server and come in unsafe way.These may have paired with C-surf bug.

**Stored Xss** – Input goes up from user and stored on the server and sent back later without proper escaping. This is also known as **Presisting cross-site scripting**. You’ll also see the cases where you able to change text on a page insert an Xss payload and exploit a user simply by waiting until they go to the page in the future.

**Dom Xss** – Input from a user is inserted into the page’s DOM without proper handling, enabling insertion of arbitrary nodes.

# Recognition

1. Figure out where data goes – If it’s stored Xss where it stored a file contents or even a file-name Does it embedded in a tag attribute or tag content. A string in the script an integer in the script. In those cases you may be able to get direct JAVA-script injection.
2. Figure out any special handling : Do URLs get turned into links
3. Figure out how special characters are handled : A good way is to input something like ’<>:;" etc. If one of them makes it through encoding make a note of that If you there are many handling in previous step make sure test that too.

If your URLs turned into links what happens when your URL’s include special characters

# Exploitation

If in special characters exploitation just use just embed anchor tag and use the image tag with onerror.

# Xss Cheatsheet

- ">

"
    
    # test
    
- ‘+alert(1)+’
- “onmouseover=”aler(1)
- http://“onmouseover=”alert(1)