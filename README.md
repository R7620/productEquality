# productEquality

package com.raj.collectionlabtask;

import java.util.Objects;

public class ProductEquality
{
	public static void main(String[]args) 
	{
		 Product p1= new Product(101, "mobile");
		 Product p2=new Product(102,"laptop");
		 p1.equals(p2);
		 System.out.println("return compare : "+ p1.equals(p2));
		 
		 
	}
	
}
 class Product 
 {
         private int product;
        private String productName;
     public Product(int product,String productName) 
    {
	this.product=product;
	this.productName=productName;
    }
     
	@Override
	public int hashCode() {
		return Objects.hash(product, productName);
	}
	
	@Override
	public boolean equals(Object obj) 
	  {
	 if(obj instanceof Product)
	 {
	 Product p2 = (Product) obj;
	 if(this.product==p2.product )
	 {
	     if(this.productName.equals(productName)) {
	    	     return true;
	     }
	     else {
	    	  return false;
	     }
	 }
	 else {
		  return false;
	 }
	 
	 }
	 else {
		  return false;
	 }
	 
	  }
	 
	


}

//	public boolean equals(Object obj) {
//		if (obj == null)
//			return false;
//		if (obj instanceof Product) {
//		Product other = (Product) obj;
//		return product == other.product && productName.equals(other.productName);
//		}
//		return false;	
//	}
     
	
