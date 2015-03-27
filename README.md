# Programming-Projects
Java Code for CSCI 1933

public class AssociationList<Key, Value>{
  private class Node{
    private Node myNext;
    private Base myValue;
    private Base myKey;
    public Node<Key, Value>(Key mKey, Value mVal, Node mNext){
      this.myNext=mNext;
      this.myValue=mVal;
      this.myKey=mKey;
      }
    public Base getVal(){
      return this.myValue;
      }
    public Base getKey(){
      return this.myKey;
      }
    public Node getNext(){
      return this.myNext;
      }
    public void setNext(Node newNext){
      this.myNext=newNext;
    }
    public void setKey(Key mKey){
      this.myKey=mKey;
      }
    public void setVal(Value mVal){
      this.myValue=mVal;
      }
  private Node head;
  public AssociationList(){
    Node newHead = new Node<Key, Value>(null,null,null);
    this.head=newHead;
    }
  public void add(Key myKey, Value myValue){
    Node newHead = new Node<Base>(myKey, myValue, head);
    head=newHead;
    }
  public Base search(Key querie){
    current=this.head;
    while(current.getKey()!=querie){
      if(current.getNext()==null){
        throw new IndexOutOfBoundsException("Value not found");
        }
      current=current.getNext();
      }
    return current.getVal();
    }
  public boolean isEmpty(){
    return this.head.getNext()==null;
    }
  public 
  
  
