---
title: "تحديث الكيان المركب لدفتر يومية البنك"
description: "تُعد الخطوات التالية مطلوبة لإضافة الحقل BankTransactionType الإضافي إلى BankJournalEntity المركب."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a8b11df3b21f8d97986d934ff3c65931aa7ee0c6
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="94211-103">تحديث الكيان المركب لدفتر يومية البنك</span><span class="sxs-lookup"><span data-stu-id="94211-103">Update the bank journal composite entity</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="94211-104">تُعد الخطوات التالية مطلوبة لإضافة الحقل BankTransactionType الإضافي إلى BankJournalEntity المركب.</span><span class="sxs-lookup"><span data-stu-id="94211-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="94211-105">استخدم الخطوات التالية لإضافة الحقل الإضافي BankTransactionType إلى BankJournalEntity المركب.</span><span class="sxs-lookup"><span data-stu-id="94211-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="94211-106">تجميع ومزامنة الكيانات المركبة التالية لدفتر يومية البنك والكيانات وجداول التشغيل المرحلي:</span><span class="sxs-lookup"><span data-stu-id="94211-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="94211-107">الكيان المركب‬\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="94211-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="94211-108">الكيان\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="94211-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="94211-109">الكيان\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="94211-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="94211-110">الجدول\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="94211-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="94211-111">الجدول\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="94211-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="94211-112">إدارة البيانات\\مشاريع البيانات</span><span class="sxs-lookup"><span data-stu-id="94211-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="94211-113">عرض نوع **الحركة البنكية** على تخطيط **المصدر المصدر**.</span><span class="sxs-lookup"><span data-stu-id="94211-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="94211-114">تنسيق بيانات المصدر = عنصر XML</span><span class="sxs-lookup"><span data-stu-id="94211-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="94211-115">اسم الكيان = دفتر يومية البنك</span><span class="sxs-lookup"><span data-stu-id="94211-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="94211-116">تحميل ملف البيانات = إصدار SampleBankJournalCompositeEntity.xml الجديد</span><span class="sxs-lookup"><span data-stu-id="94211-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="94211-117">انقر فوق **نعم** للكتابة فوق الملف الموجود.</span><span class="sxs-lookup"><span data-stu-id="94211-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="94211-118">انقر فوق **نعم** لإنشاء التعيين منذ البداية.</span><span class="sxs-lookup"><span data-stu-id="94211-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="94211-119">تأكد من تعيين "نوع الحركة البنكية".</span><span class="sxs-lookup"><span data-stu-id="94211-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="94211-120">انقر فوق **عرض الخريطة** على كيان البند.</span><span class="sxs-lookup"><span data-stu-id="94211-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="94211-121">تأكد من تعيين نوع الحركة البنكية من المصدر إلى التشغيل المرحلي‬.</span><span class="sxs-lookup"><span data-stu-id="94211-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="94211-122">استيراد كشف الحساب الجديد.</span><span class="sxs-lookup"><span data-stu-id="94211-122">Import the new statement.</span></span>





