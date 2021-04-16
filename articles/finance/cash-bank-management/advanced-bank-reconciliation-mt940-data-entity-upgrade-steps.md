---
title: الاستيراد المتقدم للتسوية البنكية MT940 - ترقية كيان بيانات مركب
description: يجب إضافة رقم تسلسلي إلى كيان استيراد كشف الحساب البنكي لدعم تنسيق MT940.
author: panolte
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d6534cc0835eabe91ab485e1d71412885d12123f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827424"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="51ce2-103">الاستيراد المتقدم للتسوية البنكية MT940 - ترقية كيان بيانات مركب</span><span class="sxs-lookup"><span data-stu-id="51ce2-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51ce2-104">يجب إضافة رقم تسلسلي إلى كيان استيراد كشف الحساب البنكي لدعم تنسيق MT940.</span><span class="sxs-lookup"><span data-stu-id="51ce2-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="51ce2-105">استخدم الخطوات التالية لإضافة كيان استيراد كشف الحساب البنكي لدعم التنسيق MT940.</span><span class="sxs-lookup"><span data-stu-id="51ce2-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="51ce2-106">تجميع ومزامنة ما يلي:</span><span class="sxs-lookup"><span data-stu-id="51ce2-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="51ce2-107">الكيان المركب\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="51ce2-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="51ce2-108">الكيان\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="51ce2-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="51ce2-109">الكيان\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="51ce2-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="51ce2-110">الكيان\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="51ce2-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="51ce2-111">الكيان\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="51ce2-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="51ce2-112">الجداول\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="51ce2-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="51ce2-113">إدارة البيانات\\مشاريع البيانات.</span><span class="sxs-lookup"><span data-stu-id="51ce2-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="51ce2-114">تحميل مشروع (مشاريع) استيراد MT940</span><span class="sxs-lookup"><span data-stu-id="51ce2-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="51ce2-115">تغيير XSLT.</span><span class="sxs-lookup"><span data-stu-id="51ce2-115">Change XSLT.</span></span>
            -   <span data-ttu-id="51ce2-116">انقر فوق **عرض الخريط**.</span><span class="sxs-lookup"><span data-stu-id="51ce2-116">Click **View map**.</span></span>
            -   <span data-ttu-id="51ce2-117">انقر فوق **عرض الخريطة** على مستند كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="51ce2-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="51ce2-118">انقر فوق **التحويلات**</span><span class="sxs-lookup"><span data-stu-id="51ce2-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="51ce2-119">احذف الملف BankReconiliation-to-Composite.xslt.</span><span class="sxs-lookup"><span data-stu-id="51ce2-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="51ce2-120">أضف إصدار BankReconiliation-to-Composite.xsl الجديد.</span><span class="sxs-lookup"><span data-stu-id="51ce2-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="51ce2-121">عرض **الرقم التسلسلي‬** على تخطيط **بيانات المصدر‬**.</span><span class="sxs-lookup"><span data-stu-id="51ce2-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="51ce2-122">تنسيق بيانات المصدر = عنصر XML.</span><span class="sxs-lookup"><span data-stu-id="51ce2-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="51ce2-123">اسم الكيان = كشوف الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="51ce2-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="51ce2-124">تحميل ملف البيانات = إصدار SampleBankCompositeEntity.xml الجديد.</span><span class="sxs-lookup"><span data-stu-id="51ce2-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="51ce2-125">انقر فوق **نعم** للكتابة فوق الملف الموجود.</span><span class="sxs-lookup"><span data-stu-id="51ce2-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="51ce2-126">انقر فوق **نعم** لإنشاء تعيين جديد.</span><span class="sxs-lookup"><span data-stu-id="51ce2-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="51ce2-127">تأكد من تعيين **SequenceNumber**.</span><span class="sxs-lookup"><span data-stu-id="51ce2-127">Verify that S **equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="51ce2-128">انقر فوق **عرض الخريطة** على كيان كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="51ce2-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="51ce2-129">تأكد من تعيين **SequenceNumber** من المصدر إلى التشغيل المرحلي‬.</span><span class="sxs-lookup"><span data-stu-id="51ce2-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="51ce2-130">استيراد كشف الحساب الجديد.</span><span class="sxs-lookup"><span data-stu-id="51ce2-130">Import the new statement.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]