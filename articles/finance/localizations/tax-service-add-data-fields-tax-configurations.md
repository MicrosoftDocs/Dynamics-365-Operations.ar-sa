---
title: إضافة حقول البيانات في تكوينات الضرائب
description: يوضح هذا الموضوع كيفيه تخصيص تكوينات الضرائب عن طريق أضافه حقول البيانات.
author: kailiang
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9d9fce81151ad70d57c69e389e238a6f9137d56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819414"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="a6734-103">إضافة حقول البيانات في تكوينات الضرائب</span><span class="sxs-lookup"><span data-stu-id="a6734-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="a6734-104">يوضح هذا الموضوع كيفيه تخصيص تكوينات الضرائب باستخدام [حقول البيانات التي تمت اضافتها إلى التكامل الضريبي](tax-service-add-data-fields-tax-integration-by-extension.md).</span><span class="sxs-lookup"><span data-stu-id="a6734-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="a6734-105">تخصيص نموذج بيانات الضرائب</span><span class="sxs-lookup"><span data-stu-id="a6734-105">Customize the tax data model</span></span>

1. <span data-ttu-id="a6734-106">في Microsoft Dynamics 365 Finance، انتقل إلى **التقارير الإلكترونية** \> **تكوينات الضرائب**.</span><span class="sxs-lookup"><span data-stu-id="a6734-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="a6734-107">في شجره التكوين، حدد **نموذج بيانات الضريبة - أوروبا**.</span><span class="sxs-lookup"><span data-stu-id="a6734-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="a6734-108">ثم في جزء الإجراء، حدد **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="a6734-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="a6734-109">في مربع حوار القائمة المنسدلة، حدد خيار **نموذج المستند الخاضع للضريبة المشتق من الاسم: نموذج بيانات الضريبة -- أوروبا، Microsoft**، وأدخل اسما لنموذج بيانات الضريبة الجديد، ثم حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="a6734-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="a6734-110">حدد نموذج البيانات الضريبية الذي أنشأته للتو، ثم في جزء الإجراءات، حدد **مصمم**.</span><span class="sxs-lookup"><span data-stu-id="a6734-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="a6734-111">قم بتوسيع شجره نموذج البيانات، وحدد **البنود**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="a6734-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="a6734-112">في مربع الحوار **إنشاء عقدة**، أدخل اسمًا، وحدد نوع الصنف، ثم حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="a6734-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="a6734-113">أضف أي أعمدة مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="a6734-113">Add any required columns.</span></span>
8. <span data-ttu-id="a6734-114">في جزء الاجراء، حدد **حفظ**، ثم حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="a6734-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="a6734-115">أغلق الصفحة واعرض الإصدار المكتمل من نموذج بياناتك الضريبية.</span><span class="sxs-lookup"><span data-stu-id="a6734-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="a6734-116">تخصيص تكوين الضريبة</span><span class="sxs-lookup"><span data-stu-id="a6734-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="a6734-117">في Finance، انتقل إلى **التقارير الإلكترونية** \> **تكوينات الضرائب**.</span><span class="sxs-lookup"><span data-stu-id="a6734-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="a6734-118">في شجره التكوين، حدد **تكوين الضريبة -- أوروبا**.</span><span class="sxs-lookup"><span data-stu-id="a6734-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="a6734-119">ثم في جزء الإجراء، حدد **إنشاء تكوين**.</span><span class="sxs-lookup"><span data-stu-id="a6734-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="a6734-120">في مربع حوار القائمة المنسدلة، حدد خيار **تكوين خدمة الضريبة المشتق من الاسم: تكوين الضريبة -- أوروبا، Microsoft**، وأدخل اسمًا لتكوين الضريبة الجديد، ثم حدد **إنشاء التكوين**.</span><span class="sxs-lookup"><span data-stu-id="a6734-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="a6734-121">حدد تكوين الضريبة الذي أنشأته للتو، ثم في جزء الإجراءات، حدد **مصمم**.</span><span class="sxs-lookup"><span data-stu-id="a6734-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="a6734-122">في قسم **الخصائص**، في حقل **نموذج البيانات**، حدد نموذج بيانات الضريبة المخصص الذي أنشأته قبل ذلك.</span><span class="sxs-lookup"><span data-stu-id="a6734-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="a6734-123">في حقل **إصدار نموذج البيانات**، حدد الإصدار المكتمل لنموذج بيانات الضريبة.</span><span class="sxs-lookup"><span data-stu-id="a6734-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="a6734-124">حدد **إضافة**، وأضف مقاييس الضريبة المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="a6734-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="a6734-125">في جزء الاجراء، حدد **حفظ**، ثم حدد **مكتمل**.</span><span class="sxs-lookup"><span data-stu-id="a6734-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="a6734-126">أغلق الصفحة واعرض الإصدار المكتمل من تكوين الضريبة.</span><span class="sxs-lookup"><span data-stu-id="a6734-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="a6734-127">تنفيذ ميزات الضريبة في تكوين الضريبة المخصص</span><span class="sxs-lookup"><span data-stu-id="a6734-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="a6734-128">في Regulatory Configuration Service (RCS)، انتقل إلى **ميزات العولمة** \> **الضريبة**.</span><span class="sxs-lookup"><span data-stu-id="a6734-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="a6734-129">حدد **إضافة**، وأدخل معلومات حول الميزة الجديدة، ثم حدد **إنشاء ميزة**.</span><span class="sxs-lookup"><span data-stu-id="a6734-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="a6734-130">في علامة التبويب **الإصدارات**، حدد الميزة، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="a6734-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="a6734-131">في علامة التبويب **عام**، في حقل **إصدار التكوين**، حدد تكوين الضريبة المخصصة وإصدارها.</span><span class="sxs-lookup"><span data-stu-id="a6734-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="a6734-132">في مربع الحوار **إدارة الأعمدة**، حدد أعمده الرأس والبند التي تريد تضمينها في مقياس الضريبة المخصص، ثم حدد زر السهم الأيمن لإضافتها إلى قائمة **الأعمدة المحددة**.</span><span class="sxs-lookup"><span data-stu-id="a6734-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>