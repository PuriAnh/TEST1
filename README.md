# TEST1
import math
def calc_f1_score (tp, fp, fn):
    #check data type
    if not isinstance(tp, int): return print("tp must be int")
    elif not isinstance(fp, int): return print("fp must be int")
    elif not isinstance(fn, int): return print("fn must be int")
    
    #check value
    if tp <= 0 or fp <= 0 or fn <= 0:
        return print("tp and fb and fb must be greater than zero")
    
    #calcu
    precision = tp/(tp+fp)
    recall = tp/(tp+fn)
    f1_score = 2*((precision*recall)/(precision+recall))
    
    #print
    print("Precision: {0}\nRecall: {1}\nF1-score: {2}".format(precision, recall, f1_score))
