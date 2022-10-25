# Project_1
def total_occurrences(s1, s2, ch):
    """
    (str, str, str) -> int
    Precondition: len(ch) == 1
    Return the total number of times that ch occurs in s1 and s2.
    >>> total_occurrences('color', 'yellow', 'l')
    3
    >>> total_occurrences('red', 'blue', 'l')
    >>> total_occurrences('green', 'purple', 'b')
    """
    list1=list(s1)
    list2=list(s2)
    s=0

    l=list1+list2
    for i in range(len(l)):
        if l[i]==ch:
            s+=1
    return s  
        