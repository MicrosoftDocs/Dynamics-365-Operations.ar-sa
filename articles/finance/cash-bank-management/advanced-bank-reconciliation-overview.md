---
title: نظرة عامة على التسوية البنكية المتقدمة
description: تشرح هذه المقالة تدفق عملية التسويات البنكية المتقدمة. تسمح ميزة التسوية البنكية المتقدمة باستيراد كشوف الحسابات البنكية التي يمكن تسويتها تلقائيًا من داخل الحركات البنكية.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b26b6e1e50e5a9b53ca6b5315de760f5bcec4769
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899387"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="5fc05-104">نظرة عامة على التسوية البنكية المتقدمة</span><span class="sxs-lookup"><span data-stu-id="5fc05-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fc05-105">تشرح هذه المقالة تدفق عملية التسويات البنكية المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="5fc05-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="5fc05-106">تسمح ميزة التسوية البنكية المتقدمة باستيراد كشوف الحسابات البنكية التي يمكن تسويتها تلقائيًا من داخل الحركات البنكية.</span><span class="sxs-lookup"><span data-stu-id="5fc05-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="5fc05-107">تتيح لك ميزة تسوية البنكية المتقدمة استيراد كشوف الحسابات البنكية.</span><span class="sxs-lookup"><span data-stu-id="5fc05-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="5fc05-108">ويمكن بعد ذلك تسوية كشف الحساب البنكي المستورد تلقائياً من داخل الحركات البنكية.</span><span class="sxs-lookup"><span data-stu-id="5fc05-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="5fc05-109">فيما يلي الخطوات في تدفق التسوية البنكية المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="5fc05-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="5fc05-110">إعداد استيراد كشف الحساب البنكي.</span><span class="sxs-lookup"><span data-stu-id="5fc05-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="5fc05-111">استيراد كشوف الحسابات البنكية من خلال إطار كيان البيانات.</span><span class="sxs-lookup"><span data-stu-id="5fc05-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="5fc05-112">هناك ثلاثة تنسيقات نموذجية لكشف البنك مضمنة في: ISO20022، وBAI2، وMT940.</span><span class="sxs-lookup"><span data-stu-id="5fc05-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="5fc05-113">يمكن توسيع الوظائف لأي تنسيق.</span><span class="sxs-lookup"><span data-stu-id="5fc05-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="5fc05-114">قم بإعداد تسلسل رقمي لاستخدامه للتسوية البنكية المتقدمة، وحدد قواعد مطابقة التسوية البنكية.</span><span class="sxs-lookup"><span data-stu-id="5fc05-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="5fc05-115">قاعدة مطابقة التسوية هي مجموعة من المعايير المستخدمة لتصفية بنود كشف الحساب البنكي وبنود الحركة البنكية في Microsoft Dynamics 365 Finance أثناء عملية التسوية.</span><span class="sxs-lookup"><span data-stu-id="5fc05-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 Finance bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="5fc05-116">واستنادًا إلى ممارسة العمل الخاصة بك، يمكنك إعداد أكثر من قاعدة مطابقة لتحسين عملية التسوية وإجرائها تلقائيًا.‬</span><span class="sxs-lookup"><span data-stu-id="5fc05-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="5fc05-117">تسوية الكشوف البنكية مع الحركات البنكية في Finance.</span><span class="sxs-lookup"><span data-stu-id="5fc05-117">Reconcile bank statements with Finance bank transactions.</span></span>
    -   <span data-ttu-id="5fc05-118">قم بإنشاء دفاتر يومية التسوية ومطابقتها تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="5fc05-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="5fc05-119">اعرض الكشوف البنكية والحركات البنكية في Finance جنبًا إلى جنب.</span><span class="sxs-lookup"><span data-stu-id="5fc05-119">View bank statements and Finance bank transactions side by side.</span></span>
    -   <span data-ttu-id="5fc05-120">وقم بترحيل الحركات البنكية في Finance تلقائياً إذا كانت تظهر في كشف بنكي ولكن لا تظهر في تطبيق Finance.</span><span class="sxs-lookup"><span data-stu-id="5fc05-120">Automatically post Finance bank transactions if they appear on a bank statement but don't appear in the Finance app.</span></span>
    -   <span data-ttu-id="5fc05-121">إنشاء كشف تسوية.</span><span class="sxs-lookup"><span data-stu-id="5fc05-121">Generate a reconciliation statement.</span></span>




