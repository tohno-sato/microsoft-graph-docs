---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new EducationRubric
{
	DisplayName = "Example Credit Rubric",
	Description = new EducationItemBody
	{
		Content = "This is an example of a credit rubric (no points)",
		ContentType = BodyType.Text,
	},
	Levels = new List<RubricLevel>
	{
		new RubricLevel
		{
			DisplayName = "Good",
			Description = new EducationItemBody
			{
				Content = "",
				ContentType = BodyType.Text,
			},
		},
		new RubricLevel
		{
			DisplayName = "Poor",
			Description = new EducationItemBody
			{
				Content = "",
				ContentType = BodyType.Text,
			},
		},
	},
	Qualities = new List<RubricQuality>
	{
		new RubricQuality
		{
			Description = new EducationItemBody
			{
				Content = "Argument",
				ContentType = BodyType.Text,
			},
			Criteria = new List<RubricCriterion>
			{
				new RubricCriterion
				{
					Description = new EducationItemBody
					{
						Content = "The essay's argument is persuasive.",
						ContentType = BodyType.Text,
					},
				},
				new RubricCriterion
				{
					Description = new EducationItemBody
					{
						Content = "The essay's argument does not make sense.",
						ContentType = BodyType.Text,
					},
				},
			},
		},
		new RubricQuality
		{
			Description = new EducationItemBody
			{
				Content = "Spelling and Grammar",
				ContentType = BodyType.Text,
			},
			Criteria = new List<RubricCriterion>
			{
				new RubricCriterion
				{
					Description = new EducationItemBody
					{
						Content = "The essay uses proper spelling and grammar with few or no errors.",
						ContentType = BodyType.Text,
					},
				},
				new RubricCriterion
				{
					Description = new EducationItemBody
					{
						Content = "The essay has numerous errors in spelling and/or grammar.",
						ContentType = BodyType.Text,
					},
				},
			},
		},
	},
};
var result = await graphClient.Education.Me.Rubrics.PostAsync(requestBody);


```