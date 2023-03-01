
class Clone {

       Node copyList(Node head) {

         Node curr = head;

            while(curr!=null){

             Node temp = curr.next;

             curr.next = new Node(curr.data);

             curr.next.next = temp;

             curr = temp;

         }

           curr = head;

            while(curr!=null){

                if(curr.next!=null) {

                curr.next.arb = curr.arb != null ? curr.arb.next : null;

            }

                

           curr = curr.next.next;

        }

            Node org = head;

            Node copy = head.next;

            Node tem = copy;

           while(org!=null){

               org.next = org.next.next;

               if(copy.next!=null){

               copy.next = copy.next.next;

               copy = copy.next;

                   

               }

               org = org.next;

               

               

           }

            

    return tem;            

    

}

 

}
