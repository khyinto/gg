using System;
using System.Collections.Generic;

namespace lulu
{
	public class Author
	{
		private string name;
		private short age;
		private string title;
		private bool mvp;
		private DateTime pubdate;

		public Author(string name, short age, string title, bool mvp, DateTime pubdate)
		{
			this.name = name;
			this.age = age;
			this.title = title;
			this.mvp = mvp;
			this.pubdate = pubdate;
		}

		public string Name
		{
			get{return name;}
			set{name = value;}
		}
		public short Age
		{
			get{return age;}
			set{age = value;}
		}
		public string BookTitle
		{
			get{return title;}
			set{title = value;}
		}
		public bool IsMVP
		{
			get{return mvp;}
			set{mvp = value;}
		}
		public DateTime PublishedDate
		{
			get{return pubdate;}
			set{pubdate = value;}
		}

	}
	class MainClass
	{
		public static void Main (string[] args)
		{
		
			List<Author> AuthorList = new List<Author> ();

			AuthorList.Add (new Author ("김국환", 35, "A progamer", true, new DateTime (2003, 7, 10)));
			AuthorList.Add (new Author ("한재현", 28, "Unlight", false, new DateTime (2013, 7, 10)));
			AuthorList.Add (new Author ("최번개", 35, "Livigen Korea", true, new DateTime (2004, 7, 10)));
			AuthorList.Add (new Author ("장거한", 35, "Glitter", false, new DateTime (2013, 1, 10)));
			AuthorList.Add (new Author ("김갑환", 35, "Kamuse", true, new DateTime (2003, 9, 19)));

		    
			foreach (var author in AuthorList) {
				Console.WriteLine ("작가 리스트", author.Name, author.Age, author.BookTitle, author.IsMVP, author.PublishedDate);
			}
		}
	}
}
