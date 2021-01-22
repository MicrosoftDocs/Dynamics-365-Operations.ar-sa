---
title: تحديث الكيان المركب لدفتر يومية البنك
description: تُعد الخطوات التالية مطلوبة لإضافة الحقل BankTransactionType الإضافي إلى BankJournalEntity المركب.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ec196600a54a2aed4565cf422dc386d6646ff524
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899632"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="ce4e8-103">تحديث الكيان المركب لدفتر يومية البنك</span><span class="sxs-lookup"><span data-stu-id="ce4e8-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce4e8-104">تُعد الخطوات التالية مطلوبة لإضافة الحقل BankTransactionType الإضافي إلى BankJournalEntity المركب.</span><span class="sxs-lookup"><span data-stu-id="ce4e8-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="ce4e8-105">استخدم الخطوات التالية لإضافة الحقل الإضافي BankTransactionType إلى BankJournalEntity المركب.</span><span class="sxs-lookup"><span data-stu-id="ce4e8-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="ce4e8-106">تجميع ومزامنة الكيانات المركبة التالية لدفتر يومية البنك والكيانات وجداول التشغيل المرحلي:</span><span class="sxs-lookup"><span data-stu-id="ce4e8-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="ce4e8-107">الكيان المركب‬\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="ce4e8-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="ce4e8-108">الكيان\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="ce4e8-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="ce4e8-109">الكيان\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="ce4e8-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="ce4e8-110">الجدول\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="ce4e8-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="ce4e8-111">الجدول\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="ce4e8-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="ce4e8-112">إدارة البيانات\\مشاريع البيانات</span><span class="sxs-lookup"><span data-stu-id="ce4e8-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="ce4e8-113">عرض نوع **الحركة البنكية** على تخطيط **المصدر المصدر**.</span><span class="sxs-lookup"><span data-stu-id="ce4e8-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="ce4e8-114">تنسيق بيانات المصدر = عنصر XML</span><span class="sxs-lookup"><span data-stu-id="ce4e8-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="ce4e8-115">اسم الكيان = دفتر يومية البنك</span><span class="sxs-lookup"><span data-stu-id="ce4e8-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="ce4e8-116">تحميل ملف البيانات = إصدار SampleBankJournalCompositeEntity.xml الجديد</span><span class="sxs-lookup"><span data-stu-id="ce4e8-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="ce4e8-117">انقر فوق **نعم** للكتابة فوق الملف الموجود.</span><span class="sxs-lookup"><span data-stu-id="ce4e8-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="ce4e8-118">انقر فوق **نعم** لإنشاء التعيين منذ البداية.</span><span class="sxs-lookup"><span data-stu-id="ce4e8-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="ce4e8-119">تأكد من تعيين "نوع الحركة البنكية".</span><span class="sxs-lookup"><span data-stu-id="ce4e8-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="ce4e8-120">انقر فوق **عرض الخريطة** على كيان البند.</span><span class="sxs-lookup"><span data-stu-id="ce4e8-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="ce4e8-121">تأكد من تعيين نوع الحركة البنكية من المصدر إلى التشغيل المرحلي‬.</span><span class="sxs-lookup"><span data-stu-id="ce4e8-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="ce4e8-122">استيراد كشف الحساب الجديد.</span><span class="sxs-lookup"><span data-stu-id="ce4e8-122">Import the new statement.</span></span>



