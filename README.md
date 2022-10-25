# Project_1
def dyvo_insert(sentence, flag):
    """
    (str, str) -> str
    Function inserts word "диво" before every word that starts with flag.

    >>> dyvo_insert("Кит кота по хвилях катав - кит у воді, кіт на киті", "ки")
    'дивокит кота по хвилях катав - дивокит у воді, кіт на дивокиті'
    >>> dyvo_insert("Босий хлопець сіно косить, роса росить ноги босі.", "сі")
    'босий хлопець дивосіно косить, роса росить ноги босі.'
    >>> dyvo_insert("кит", "ки")
    'дивокит'
    """
    if isinstance(sentence, str) and isinstance(flag, str):
        sentence = sentence.lower()
        if sentence.startswith(flag):
            output_sentence = ("диво"+flag).join(sentence.split("" + flag))
        else:
            output_sentence = (" диво"+flag).join(sentence.split(" " + flag))
    return output_sentence


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
        