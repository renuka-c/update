# update in mongodb
import org.bson.Document;

import com.mongodb.MongoClient;
import com.mongodb.client.MongoCollection;
import com.mongodb.client.MongoDatabase;

public class MongoDb {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
          MongoClient mongoClient = new MongoClient("localhost", 27017);
	  Mongoclient mongoClient = new MongoClient("localhost", 27018);
          System.out.println("Successfully connted to MongoDB");
          
          MongoDatabase sl = mongoClient.getDatabase("Instagram");
          System.out.println("Is cereated successfully");
          
          MongoCollection<Document> collection = sl.getCollection("Users");
          System.out.println("Created Collection Successfully");
          
          Document doc = new Document("name", "Renuka");
          doc.append("age","25");
          doc.append("followers", "1200000");
          doc.append("following", "1000");
          doc.append("posts", "12000");
          doc.append("status", "private");
          collection.insertOne(doc);
          System.out.println("Inserted Completed");
          
          
          Document doc1 = new Document("name", "Naga Lakshmi");
          doc1.append("age","22");
          doc1.append("followers", "300000");
          doc1.append("following", "100");
          doc1.append("posts", "4000");
          doc1.append("status", "private");
          collection.insertOne(doc1);
          System.out.println("Inserted Completed");
          
          Document doc2 = new Document("name", "Veekshu");
          doc2.append("age","13");
          doc2.append("followers", "250");
          doc2.append("following", "99");
          doc2.append("posts", "100");
          doc2.append("status", "public");
          collection.insertOne(doc2);
          System.out.println("Inserted Completed");
          
          Document doc3 = new Document("name", "Charan");
          doc3.append("age","10");
          doc3.append("followers", "45");
          doc3.append("following", "5");
          doc3.append("posts", "12");
          doc3.append("status", "public");
          collection.insertOne(doc3);
          System.out.println("Inserted Completed");
          
          
          Document doc4 = new Document("name", "Revanth");
          doc4.append("age","23");
          doc4.append("followers", "45000");
          doc4.append("following", "1000");
          doc4.append("posts", "1200");
          doc4.append("status", "private");
          collection.insertOne(doc4);
          System.out.println("Inserted Completed");
          
          Document doc5 = new Document("name", "Nani");
          doc5.append("age","25");
          doc5.append("followers", "14000");
          doc5.append("following", "2000");
          doc5.append("posts", "450");
          doc5.append("status", "public");
          collection.insertOne(doc5);
          System.out.println("Inserted Completed");
          
          
          
          
          
	}

}

